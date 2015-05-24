## Processing the data

### Data source

This processing code will work as long as you have either a subirectory of the 
current directory named "UCI HAR Dataset" with the data files in the 
unmodified sub-directories or you have a file in the current directory named
"getdata-projectfiles-UCI HAR Dataset.zip"

In the later case the file will be unzipped by the processing code.

### Processing


# If the data directory does not exist and the raw data file does, then
# unzip the raw data file.
#
if(!file.exists(dataDirectory) && file.exists(rawDataFile)) {
    unzip(rawDataFile)
}

# Appropriately label the data set with descriptive variable names.
#
# We're going to read in the list of feature names and then use that as the
# column names for reading in the data.  That will start eah column off with
# a descriptive name, and let us use a regex match for selecting a set of
# columns later.
#
features <- read.table(file.path(dataDirectory, "features.txt"),
                       col.names=c("feature.id","feature"),
                       sep="")

# Now we'll read in the test & training sets...
#
trainset <- read.table(file.path(dataDirectory, "train", "X_train.txt"),
                       sep="",
                       col.names=features$feature)

testset <- read.table(file.path(dataDirectory, "test", "X_test.txt"), sep="",
                       col.names=features$feature)

# And simply concatentate them.  There's no overlap in the subject ids, so we'll
# end up with the proper number of rows...
#
rawdata <- rbind(testset,trainset)

# Extract the measurements on the mean and standard deviation for each
# measurement.
#
# We know that the column names for mean values have a segment that says:
# "mean...", and the std deviation columns match "std...", so we'll just do a
# regular expression match on those.

# We're only trying to get the columns which were computed ( either mean() or 
std() from measurements )
#
dataset <- select(rawdata, matches("(mean|std)\\.\\.($|\\.)"))

# Use descriptive activity names to name the activities in the data set...
#
# We'll get the activity labels from activity_labels.txt and turn activities
# into a factor variable.
#
activity_labels <- read.table(file.path(dataDirectory, "activity_labels.txt"),
                              col.names=c("activity.id", "activity"),
                              stringsAsFactors=FALSE)

trainy <- read.table(file.path(dataDirectory, "train", "y_train.txt"),
                     col.names=c("activity"),
                     sep="")

trainy$activity <- factor(trainy$activity, labels=activity_labels$activity)

testy <- read.table(file.path(dataDirectory, "test", "y_test.txt"),
                    col.names=c("activity"),
                    sep="")

testy$activity <- factor(testy$activity, labels=activity_labels$activity)

testsubj <- read.table(file.path(dataDirectory, "test", "subject_test.txt"),
                       col.names=c("subject.id"),
                       sep="")

trainsubj <- read.table(file.path(dataDirectory, "train", "subject_train.txt"),
                        col.names=c("subject.id"),
                        sep="")

allsubjects <- rbind(testsubj,trainsubj)
allactivity <- rbind(testy,trainy)

# Now we'll aggregate the data by subject ID and by activity using mean()
#
# This will add columns for those two values to the dataset in the process, so
# we didin't need to add the subjects and activities earlier.
tidyset <- aggregate(dataset, list(subject.id=allsubjects$subject.id,
                                  activity=allactivity$activity), mean)

# Now we'll save out the tidy data set...  TO read this back in use read.table
# with header = TRUE.
#
write.table(tidyset, "tidy_data_set.txt", row.names=FALSE)
