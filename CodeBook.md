# About the script

run_analysis.R is a script that transforms the original data set by performing five steps.

1.  Merges the training and the test sets to create one data set.

    -   Data is downloaded to /data/UCI HAR Dataset/ folder.

2.  Extracts only the measurements on the mean and standard deviation for each measurement.

3.  Uses descriptive activity names to name the activities in the data set

4.  Appropriately labels the data set with descriptive variable names.

5.  From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.

# The variables

features \<- features.txt The features selected for this database come from the accelerometer and gyroscope 3-axial raw signals tAcc-XYZ and tGyro-XYZ.

activities \<- activity_labels.txt List of activities performed when the corresponding measurements were taken and its codes (labels)

subject_test \<- test/subject_test.txtcontains test data of 9/30 volunteer test subjects being observed

x_test \<- test/X_test.txt contains recorded features test data

y_test \<- test/y_test.txtcontains test data of activities'code labels

subject_train \<- test/subject_train.txtcontains train data of 21/30 volunteer subjects being observed

x_train \<- test/X_train.txtcontains recorded features train data

y_train \<- test/y_train.txtcontains train data of activities'code labels

## Merging Test and Train data

rbind() function is used to

-   merge x_train and x_test as X

-   merge y_train and y_test as Y

-   merge subject_train and subject_test as Subject

Merged_Data merges Subject, X, and Y using cbind() function

# Others

1.  Only mean and standard deviation measures were extracted as TidyData which is a subset of Merged_Data

2.  Data sets were labeled with descriptive variable names.

-   code column in TidyData renamed into activities

-   All Acc in column's name replaced by Accelerometer

-   All Gyro in column's name replaced by Gyroscope

-   All BodyBody in column's name replaced by Body

-   All Mag in column's name replaced by Magnitude

-   All start with character f in column's name replaced by Frequency

-   All start with character t in column's name replaced by Time

# Final Data

TidyData is summarized as FinalData.
