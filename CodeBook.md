## Code Book


### ID fields

#### subject.id                  

- The ID number of the subject performing the action.  IDs range from 1 to 30.

#### activity

- The activity being performed.  Valid activity values are:<br>
1 WALKING<br>
2 WALKING_UPSTAIRS<br>
3 WALKING_DOWNSTAIRS<br>
4 SITTING<br>
5 STANDING<br>
6 LAYING<br>
    
### Signals

The value of each signal field has been normalized, and is bounded in [-1,1].

#### tBodyAcc.mean...X        
#### tBodyAcc.mean...Y           
#### tBodyAcc.mean...Z

- The mean values of the X, Y and Z components of the body acceleration signal 
from the accelerometer, which was extracted from the raw acceleration signal using 
a low-pass filter.

#### tBodyAcc.std...X  
#### tBodyAcc.std...Y
#### tBodyAcc.std...Z

- The standard deviations of the X, Y and Z components of the raw body acceleration signal 
from the accelerometer, which was extracted from the raw acceleration signal using 
a low-pass filter.

#### tGravityAcc.mean...X
#### tGravityAcc.mean...Y
#### tGravityAcc.mean...Z

- The mean values of the X, Y and Z components of the gravitational acceleration signal 
from the accelerometer, which was extracted from the raw acceleration signal using 
a low-pass filter.

#### tGravityAcc.std...X
#### tGravityAcc.std...Y
#### tGravityAcc.std...Z

- The standard deviations of the X, Y and Z components of the gravitational 
acceleration signal from the accelerometer, which was extracted from the raw 
acceleration signal using 
a low-pass filter.

#### tBodyAccJerk.mean...X
#### tBodyAccJerk.mean...Y
#### tBodyAccJerk.mean...Z

- The mean values of the X, Y and Z components of the body acceleration jerk, 
which was calculated by deriving the body acceleration value in time.

#### tBodyAccJerk.std...X
#### tBodyAccJerk.std...Y
#### tBodyAccJerk.std...Z

- The standard deviations of the X, Y and Z components of the body acceleration jerk, 
which was calculated by deriving the body acceleration value in time.

#### tBodyGyro.mean...X
#### tBodyGyro.mean...Y
#### tBodyGyro.mean...Z

- The mean values of the X, Y and Z components of the gyroscope signal.

#### tBodyGyro.std...X
#### tBodyGyro.std...Y
#### tBodyGyro.std...Z

- The standard deviations of the X, Y and Z components of the gyroscope signal.

#### tBodyGyroJerk.mean...X
#### tBodyGyroJerk.mean...Y
#### tBodyGyroJerk.mean...Z

- The mean values of the X, Y and Z components of the gyroscope jerk, 
which was calculated by deriving the gyroscope signal in time.

#### tBodyGyroJerk.std...X
#### tBodyGyroJerk.std...Y
#### tBodyGyroJerk.std...Z

- The standard deviations of the X, Y and Z components of the gyroscope jerk, 
which was calculated by deriving the gyroscope signal in time.

#### tBodyAccMag.mean..        

- The mean value of the magnitude of the body acceleration signal.  The magnitude was 
calculated from the tBodyAcc X, Y & Z components using the Euclidean norm.

#### tBodyAccMag.std..

- The standard deviation of the magnitude of the body acceleration signal.  The magnitude was 
calculated from the tBodyAcc X, Y & Z components using the Euclidean norm.

#### tGravityAccMag.mean..

- The mean value of the magnitude of the gravitational acceleration signal.  
The magnitude was calculated from the tGravityAcc X, Y & Z components using 
the Euclidean norm.

#### tGravityAccMag.std..

- The standard deviation of the magnitude of the gravitational  acceleration signal.  
The magnitude was calculated from the tGravityAcc X, Y & Z components using the 
Euclidean norm.

#### tBodyAccJerkMag.mean..

- The mean value of the magnitude of the body acceleration jerk.  The magnitude was 
calculated from the tBodyAccJerk X, Y & Z components using the Euclidean norm.

#### tBodyAccJerkMag.std..

- The standard deviation of the magnitude of the body acceleration jerk.  The magnitude 
was calculated from the tBodyAccJerk X, Y & Z components using the Euclidean norm.

#### tBodyGyroMag.mean..        

- The mean value of the magnitude of the gyroscope signal.  The magnitude was 
calculated from the tBodyGyro X, Y & Z components using the Euclidean norm.

#### tBodyGyroMag.std..

- The standard deviation of the magnitude of the gyroscope signal.  The magnitude was 
calculated from the tBodyGyro X, Y & Z components using the Euclidean norm.

#### tBodyGyroJerkMag.mean..

- The mean value of the magnitude of the gyroscope jerk.  The magnitude was 
calculated from the tBodyGyroJerk X, Y & Z components using the Euclidean norm.

#### tBodyGyroJerkMag.std..

- The standard deviation of the magnitude of the gyroscope jerk.  The magnitude 
was calculated from the tBodyGyroJerk X, Y & Z components using the Euclidean norm.

### FFT Values

The rest of the values were calculated by applying a Fast Fourier Transform (FFT) to 
the corresponding signal.  

#### fBodyAcc.mean...X
#### fBodyAcc.mean...Y
#### fBodyAcc.mean...Z

- The mean of the X, Y and Z components of the FFT of body acceleration.

#### fBodyAcc.std...X
#### fBodyAcc.std...Y
#### fBodyAcc.std...Z

- The standard deviation of the X, Y and Z components of the FFT of body acceleration.

#### fBodyAccJerk.mean...X
#### fBodyAccJerk.mean...Y
#### fBodyAccJerk.mean...Z

- The mean of the X, Y and Z components of the FFT of body acceleration jerk.

#### fBodyAccJerk.std...X
#### fBodyAccJerk.std...Y
#### fBodyAccJerk.std...Z

- The standard deviation of the X, Y and Z components of the FFT of body 
acceleration jerk.

#### fBodyGyro.mean...X
#### fBodyGyro.mean...Y
#### fBodyGyro.mean...Z

- The mean of the X, Y and Z components of the FFT of body gyroscope.

#### fBodyGyro.std...X
#### fBodyGyro.std...Y
#### fBodyGyro.std...Z

- The standard deviation of the X, Y and Z components of the FFT of body 
gyroscope.

#### fBodyAccMag.mean..

- The mean of the FFT of the magnitude of body acceleration.

#### fBodyAccMag.std..

- The standard deviation of the FFT of the magnitude of body acceleration.

#### fBodyBodyAccJerkMag.mean..

- The mean of the FFT of the magnitude of body acceleration jerk.

#### fBodyBodyAccJerkMag.std..

- The standard deviation of the FFT of the magnitude of body acceleration jerk.

#### fBodyBodyGyroMag.mean..

- The mean of the FFT of the magnitude of body gyroscope.

#### fBodyBodyGyroMag.std..

- The standard deviation of the FFT of the magnitude of body gyroscope.

#### fBodyBodyGyroJerkMag.mean..

- The mean of the FFT of the magnitude of body gyroscope jerk.

#### fBodyBodyGyroJerkMag.std..

- The standard deviation of the FFT of the magnitude of body gyroscope jerk.


