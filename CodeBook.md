# Code Book

## The Data
	The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. 
	Using its embedded accelerometer (Acc) and gyroscope (Gyro), we captured 3-axial linear acceleration (X, Y, and Z) and 3-axial angular velocity (X, Y, and Z) at a constant rate of 50Hz.The sensor acceleration signal (from the accelerometer and gyroscope), which has gravitational (Gravity) and body (Body) motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time (t) and frequency domain (f).
	Subsequently, the body linear acceleration and angular velocity were derived in time to obtain Jerk signals (Jerk). Also the magnitude of these three-dimensional signals were calculated using the Euclidean norm (Mag).
	The data only present the mean and standard deviation for each variable per subject and per activity.

## Data Dictionary

activity	1
	Activities measured
		(Categorical)
		walking            
		walking_upstairs   
		walking_downstairs
		sitting            
		standing           
		laying   
		
subject		2
	Indiduals who participate from the experiment 
		(numeric - ordenal) 1...30

tBodyAccMeanX	3
	The mean of the body acceleration signal obtained by subtracting the gravity from the total acceleration in the X axis in standard gravity units 'g' by time.
		(numeric - continuous)

tBodyAccMeanY	4
	The mean of the body acceleration signal obtained by subtracting the gravity from the total acceleration in the Y axis in standard gravity units 'g' by time.
		(numeric - continuous)
 
tBodyAccMeanZ	5
	The mean of the body acceleration signal obtained by subtracting the gravity from the total acceleration in the Z axis in standard gravity units 'g' by time.
		(numeric - continuous)
 
tBodyAccStdX	6 
	The stardard deviation of the body acceleration signal obtained by subtracting the gravity from the total acceleration in the X axis in standard gravity units 'g' by time.
		(numeric - continuous)

tBodyAccStdY	7 
	The stardard deviation of the body acceleration signal obtained by subtracting the gravity from the total acceleration in the Y axis in standard gravity units 'g' by time.
		(numeric - continuous)

tBodyAccStdZ	8 
	The stardard deviation of the body acceleration signal obtained by subtracting the gravity from the total acceleration in the Z axis in standard gravity units 'g' by time.
		(numeric - continuous)

tGravityAccMeanX	9
	The mean of the gravity acceleration signal obtained in the X axis in standard gravity units 'g' by time.
		(numeric - continuous)

tGravityAccMeanY	10
	The mean of the gravity acceleration signal obtained in the Y axis in standard gravity units 'g' by time.
		(numeric - continuous)
  
tGravityAccMeanZ	11 
	The mean of the gravity acceleration signal obtained in the Z axis in standard gravity units 'g' by time.
		(numeric - continuous)

tGravityAccStdX	12
	The standard deviation of the gravity acceleration signal obtained in the X axis in standard gravity units 'g' by time.
		(numeric - continuous)
 
tGravityAccStdY	13
	The standard deviation of the gravity acceleration signal obtained in the Y axis in standard gravity units 'g' by time.
		(numeric - continuous)
 
tGravityAccStdZ	14 
	The standard deviation of the gravity acceleration signal obtained in the Z axis in standard gravity units 'g' by time.
		(numeric - continuous)
 
tBodyAccJerkMeanX	15 
	 The mean of the body acceleration signal obtained by subtracting the gravity from the total acceleration in the X axis in standard gravity units 'g' derived in time.
		(numeric - continuous)

tBodyAccJerkMeanY	16
	 The mean of the body acceleration signal obtained by subtracting the gravity from the total acceleration in the Y axis in standard gravity units 'g' derived in time.
		(numeric - continuous)

tBodyAccJerkMeanZ	17
	 The mean of the body acceleration signal obtained by subtracting the gravity from the total acceleration in the Z axis in standard gravity units 'g' derived in time.
		(numeric - continuous)

tBodyAccJerkStdX	18
	 The standard deviation of the body acceleration signal obtained by subtracting the gravity from the total acceleration in the X axis in standard gravity units 'g' derived in time.
		(numeric - continuous)

tBodyAccJerkStdY	19
	 The standard deviation of the body acceleration signal obtained by subtracting the gravity from the total acceleration in the Y axis in standard gravity units 'g' derived in time.
		(numeric - continuous)

tBodyAccJerkStdZ	20
	 The standard deviation of the body acceleration signal obtained by subtracting the gravity from the total acceleration in the Z axis in standard gravity units 'g' derived in time.
		(numeric - continuous)

tBodyGyroMeanX	21
	The mean of the angular velocity vector measured by the gyroscope in the X axis by time. The units are radians/second.
		(numeric - continuous)

tBodyGyroMeanY	22
	The mean of the angular velocity vector measured by the gyroscope in the Y axis by time. The units are radians/second.
		(numeric - continuous)

tBodyGyroMeanZ	23
	The mean of the angular velocity vector measured by the gyroscope in the Z axis by time. The units are radians/second.
		(numeric - continuous)

tBodyGyroStdX	24
	The standard deviation of the angular velocity vector measured by the gyroscope in the X axis by time. The units are radians/second.
		(numeric - continuous)

tBodyGyroStdY	25
	The standard deviation of the angular velocity vector measured by the gyroscope in the Y axis by time. The units are radians/second.	
		(numeric - continuous)

tBodyGyroStdZ	26
	The standard deviation of the angular velocity vector measured by the gyroscope in the Z axis by time. The units are radians/second. 
		(numeric - continuous)

tBodyGyroJerkMeanX	27 
	The mean of the angular velocity vector measured by the gyroscope in the X axis derived in time. The units are radians/second.
		(numeric - continuous)

tBodyGyroJerkMeanY	28
	The mean of the angular velocity vector measured by the gyroscope in the Y axis derived in time. The units are radians/second.
		(numeric - continuous)
 
tBodyGyroJerkMeanZ	29 
	The mean of the angular velocity vector measured by the gyroscope in the Z axis derived in time. The units are radians/second.
		(numeric - continuous)

tBodyGyroJerkStdX	30
	The standard deviation of the angular velocity vector measured by the gyroscope in the X axis derived in time. The units are radians/second.
		(numeric - continuous)
 
tBodyGyroJerkStdY	31
	The standard deviation of the angular velocity vector measured by the gyroscope in the X axis derived in time. The units are radians/second.
		(numeric - continuous)
  
tBodyGyroJerkStdZ	32 
	The standard deviation of the angular velocity vector measured by the gyroscope in the X axis derived in time. The units are radians/second.
		(numeric - continuous)
 
tBodyAccMagMean	33
	The mean of the magnitude of body acceleration signal obtained by subtracting the gravity from the total acceleration in standard gravity units 'g' using Euclidean norm by time.
		(numeric - continuous)
  
tBodyAccMagStd	34
	The standard deviation of the magnitude of body acceleration signal obtained by subtracting the gravity from the total acceleration in standard gravity units 'g' using Euclidean norm by time.
		(numeric - continuous)
  
tGravityAccMagMean	35
	The mean of the magnitude of gravity acceleration signal obtained in standard gravity units 'g' using Euclidean norm by time.
		(numeric - continuous)
   
tGravityAccMagStd	36 
	The standard deviation of the magnitude of gravity acceleration signal obtained in standard gravity units 'g' using Euclidean norm by time.
		(numeric - continuous)
  
tBodyAccJerkMagMean	37
	The mean of the magnitude of body acceleration signal obtained by subtracting the gravity from the total acceleration in standard gravity units 'g' using Euclidean norm derived in time.
		(numeric - continuous)
   
tBodyAccJerkMagStd	38
	The standard deviation of the magnitude of body acceleration signal obtained by subtracting the gravity from the total acceleration in standard gravity units 'g' using Euclidean norm derived in time.
		(numeric - continuous)
   
tBodyGyroMagMean	39
	The mean of the magnitude of angular velocity vector measured by the gyroscope using Euclidean norm. The units are radians/second. 
		(numeric - continuous)
 
tBodyGyroMagStd	40
	The standard deviation of the magnitude of angular velocity vector measured by the gyroscope using Euclidean norm. The units are radians/second. 
		(numeric - continuous)
  
tBodyGyroJerkMagMean	41 
	The mean of the magnitude of angular velocity vector measured by the gyroscope using Euclidean normderived in time. The units are radians/second. 
		(numeric - continuous)
 
tBodyGyroJerkMagStd	42
	The standard deviation of the magnitude of angular velocity vector measured by the gyroscope using Euclidean normderived in time. The units are radians/second. 
		(numeric - continuous)
  
fBodyAccMeanX	43
	The mean of the body acceleration signal obtained by subtracting the gravity from the total acceleration in the X axis in standard gravity units 'g' by frequency.
		(numeric - continuous)
 
fBodyAccMeanY	44
	The mean of the body acceleration signal obtained by subtracting the gravity from the total acceleration in the Y axis in standard gravity units 'g' by frequency.
		(numeric - continuous)
  
fBodyAccMeanZ	45 
	The mean of the body acceleration signal obtained by subtracting the gravity from the total acceleration in the Z axis in standard gravity units 'g' by frequency.
		(numeric - continuous)
 
fBodyAccStdX	46
	The standard deviation of the body acceleration signal obtained by subtracting the gravity from the total acceleration in the X axis in standard gravity units 'g' by frequency.
		(numeric - continuous)
  
fBodyAccStdY	47
	The standard deviation of the body acceleration signal obtained by subtracting the gravity from the total acceleration in the Y axis in standard gravity units 'g' by frequency.
		(numeric - continuous)
  
fBodyAccStdZ	48 
	The standard deviation of the body acceleration signal obtained by subtracting the gravity from the total acceleration in the Z axis in standard gravity units 'g' by frequency.
		(numeric - continuous)
 
fBodyAccJerkMeanX	49
	 The mean of the body acceleration signal obtained by subtracting the gravity from the total acceleration in the X axis in standard gravity units 'g' derived in time by frequency.
		(numeric - continuous)
 
fBodyAccJerkMeanY	50 
	 The mean of the body acceleration signal obtained by subtracting the gravity from the total acceleration in the Y axis in standard gravity units 'g' derived in time by frequency.
		(numeric - continuous)
 
fBodyAccJerkMeanZ	51 
	 The mean of the body acceleration signal obtained by subtracting the gravity from the total acceleration in the Z axis in standard gravity units 'g' derived in time by frequency.
		(numeric - continuous)
 
fBodyAccJerkStdX	52
	 The standard deviation of the body acceleration signal obtained by subtracting the gravity from the total acceleration in the X axis in standard gravity units 'g' derived in time by frequency.
		(numeric - continuous)
  
fBodyAccJerkStdY	53 
	 The standard deviation of the body acceleration signal obtained by subtracting the gravity from the total acceleration in the Y axis in standard gravity units 'g' derived in time by frequency.
		(numeric - continuous)
 
fBodyAccJerkStdZ	54
	 The standard deviation of the body acceleration signal obtained by subtracting the gravity from the total acceleration in the Z axis in standard gravity units 'g' derived in time by frequency.
		(numeric - continuous)
  
fBodyGyroMeanX	55 
	The mean of the angular velocity vector measured by the gyroscope in the X axis by frequency. The units are radians/second.
		(numeric - continuous)

fBodyGyroMeanY	56
	The mean of the angular velocity vector measured by the gyroscope in the Y axis by frequency. The units are radians/second.
		(numeric - continuous)
 
fBodyGyroMeanZ	57
	The mean of the angular velocity vector measured by the gyroscope in the Z axis by frequency. The units are radians/second.
		(numeric - continuous)
 
fBodyGyroStdX	58
	The standard deviation of the angular velocity vector measured by the gyroscope in the X axis by frequency. The units are radians/second.
		(numeric - continuous)
 
fBodyGyroStdY	59
	The standard deviation of the angular velocity vector measured by the gyroscope in the Y axis by frequency. The units are radians/second.
		(numeric - continuous)
 
fBodyGyroStdZ	60
	The standard deviation of the angular velocity vector measured by the gyroscope in the Z axis by frequency. The units are radians/second.
		(numeric - continuous)
 
fBodyAccMagMean	61
	The mean of the magnitude of body acceleration signal obtained by subtracting the gravity from the total acceleration in standard gravity units 'g' using Euclidean norm by frequency.
		(numeric - continuous)
   
fBodyAccMagStd	62
	The standard deviation of the magnitude of body acceleration signal obtained by subtracting the gravity from the total acceleration in standard gravity units 'g' using Euclidean norm by frequency.
		(numeric - continuous)
  
fBodyBodyAccJerkMagMean	63
	The mean of the magnitude of body acceleration signal obtained by subtracting the gravity from the total acceleration in standard gravity units 'g' using Euclidean norm derived in time by frequency.
		(numeric - continuous)
   
fBodyBodyAccJerkMagStd	64 
	The standard deviation of the magnitude of body acceleration signal obtained by subtracting the gravity from the total acceleration in standard gravity units 'g' using Euclidean norm derived in time by frequency.
		(numeric - continuous)
   
fBodyBodyGyroMagMean	65
	The mean of the magnitude of angular velocity vector measured by the gyroscope using Euclidean norm by frequency. The units are radians/second. 
		(numeric - continuous)
  
fBodyBodyGyroMagStd	66 
	The standard deviation of the magnitude of angular velocity vector measured by the gyroscope using Euclidean norm by frequency. The units are radians/second. 
		(numeric - continuous)
  
fBodyBodyGyroJerkMagMean	67
	The mean of the magnitude of angular velocity vector measured by the gyroscope using Euclidean norm derived in time by frequency. The units are radians/second. 
		(numeric - continuous)
 
fBodyBodyGyroJerkMagStd	68
	The standard deviation of the magnitude of angular velocity vector measured by the gyroscope using Euclidean normderived in time by frequency. The units are radians/second. 
		(numeric - continuous)
  