Code Book

Please refer to the following URL to see the code book for the original dataset used in this work. 

http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

The remainder of this codebook shows how we transform that data to create a tidy data set as specified in the course instructins. 

1. Read data and merge

subject_test : subject IDs for test

subject_train : subject IDs for train

x_test : values of variables in test

x_train : values of variables in train

y_test : activity ID in test

y_train : activity ID in train

activity_labels : Description of activity IDs in y_test and y_train

features : description(label) of each variables in X_test and X_train

dataSubject : merge of subject_train, subject_test

dataActivity : merge of activity_train, dataActivityTest

dataFeatures: merge of features_train, features_test

2. Extract only mean() and std()

Create a vector of only mean and std labels, then use the vector to subset dataSet.

selectedNames : a vector of only mean and std labels extracted from 2nd column of features

Data : at the end of this step, dataSet will only contain mean and std variables

3. Changing column labels of Data

Create more meaningful column names for:

^t to time
^f to frequency
Acc to Accelerometer
Gyro to Gyroscope
Mag to Magnitude
BodyBody to Body

4. Adding Subject and Activity to the dataSet

Combine test data and train data of subject and activity, then give descriptive lables. Finally, bind with Data. At the end of this step, Data has 2 additonal columns 'subject' and 'activity' in the left side.

subject : bind of subject_train and subject_test
activity : bind of y_train and y_test

5. Output tidy data

tidydata : tidy dataset
