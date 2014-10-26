##Code Book for Getting and Cleaning Data Course Project
This code book describes the variables, the data, and the transformations performed to clean up the data and generate the required tidy data set.

####Source Data Information
This data set contains data collected from the accelerometers from a Samsung Galaxy S II smartphone, for the experiments carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each volunteer performed 6 activities and the 3-axial linear acceleration and 3-axial angular velocity were captured at a constant rate of 50Hz. Full details of the input data can be found at the site where the source data was obtained:
[http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones] (http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones)

####The Dataset
The dataset contains the following files:
* 'README.txt': Description of the dataset
* 'features_info.txt': Contains information about the variables used on the feature vector
* 'features.txt': List of all features
* 'activity_labels.txt': Links the class labels with their activity names
* 'train/X_train.txt': Training set
* 'train/Y_train.txt': Training labels
* 'test/X_test.txt': Test set
* 'test/Y_test.txt': Test labels

The following files are available for the train and test data. 
* 'train/subject_train.txt': Each row identifies the subject who performed the activity for each window sample. Its range is from 1 to 30
* 'train/Inertial Signals/total_acc_x_train.txt': The acceleration signal from the smartphone accelerometer X axis in standard gravity units 'g'. Every row shows a 128 element vector. The same description applies for the 'total_acc_y_train.txt' and 'total_acc_z_train.txt' files for the Y and Z axis.
* 'train/Inertial Signals/body_acc_x_train.txt': The body acceleration signal obtained by subtracting the gravity from the total acceleration
* 'train/Inertial Signals/body_gyro_x_train.txt': The angular velocity vector measured by the gyroscope for each window sample. The units are radians/second.

####Transformation Performed
Five steps involved in the transformation process:

1. Merges the training and the test sets to create one data set.
2. Extracts only the measurements on the mean and standard deviation for each measurement.
3. Uses descriptive activity names to name the activities in the data set
4. Appropriately labels the data set with descriptive activity names.
5. Creates a second, independent tidy data set with the average of each variable for each activity and each subject.

####Description of the script run_analysis.R

1. Requires reshapre2 and data.table librareis.
2. Loads both test and train data
3. Loads the features and activity labels.
4. Extracts the mean and standard deviation column names and data.
5. Processes the data. There are two parts processing test and train data respectively.
6. Merges data set.
