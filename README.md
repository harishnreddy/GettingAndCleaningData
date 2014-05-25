### Introduction

The purpose of the run_analysis script was to take accelerometer and gyroscope
data collected from 30 subjects and aggregate the means for the various measurements
by subject and activity

Because the final use case of the data was unclear, the author decided to take
all of the measurements that had means and standard deviation associated with it 
and subset it.  

Once more detail on the actual use of the data is provided, then the actual columns
to retrieve and calculations to perform can be revisited.

### The high level algorithm was as follows

1. consolidate subject training and test data

2. consolidate activity training and test data

make activity information more descriptive by makeing following conversions

1. 1 - walking
2. 2 - walking upstairs
3. 3 - walking downstairs
4. 4 - sitting
5. 5 - standing
6. 6 - laying


3. cosolidate measurement training and test data

a. rename variables
b. consolidate variables to just mean and standard deviation variables

VARIABLE -> COLUMN IN DATASET
tBodyAcc-XYZ  	- 1-6
tGravityAcc-XYZ		- 41-46
tBodyAccJerk-XYZ	- 81-86
tBodyGyro-XYZ		- 121-126
tBodyGyroJerk-XYZ	- 161-166
tBodyAccMag		- 201-202
tGravityAccMag		- 214-215
tBodyAccJerkMag		- 227-228
tBodyGyroMag		- 240-241
tBodyGyroJerkMag	- 253-254
fBodyAcc-XYZ		- 266-271
fBodyAccJerk-XYZ	- 345-350
fBodyGyro-XYZ		- 424-429
fBodyAccMag		- 503-504
fBodyAccJerkMag		- 516-517
fBodyGyroMag		- 529-530
fBodyGyroJerkMag	- 542-543

4. consolidate 3 sets of data into one dataframe

5. calculate mean of all means and standard deviation of all columns aggregated by
subject and activity

6. clean up column names for readability

7. save as csv file
