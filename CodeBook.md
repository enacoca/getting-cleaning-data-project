Getting and Cleaning Data Course Project CodeBook

This file describes the variables, the data, and any transformations or work to be performed to clean up the data.

The site where the data was obtained:
http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

The data for the project:
https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

The run_analysis.R script performs the following steps to clean the data:

1) Read X_train.txt, y_train.txt and subject_train.txt from the "./data/train" folder and store them in trainData, trainLabel and trainSubject variables respectively.
2) Read X_test.txt, y_test.txt and subject_test.txt from the "./data/test" folder and store them in testData, testLabel and testsubject variables respectively.

3) Read the features.txt file from the "/data" folder and store the data in a variable called features. 

4) Clean the column names of the subset. We remove the "()" and "-" symbols in the names, as well as make the first letter of "mean" and "std" a capital letter "M" and "S" respectively.

5)Read the activity_labels.txt file from the "./data"" folder and store the data in a variable called activity.Clean the activity names in the second column of activity. 
6) Transform the values of joinLabel according to the activity data frame.
7 ) Combine the joinSubject, joinLabel and joinData by column. Name the first two columns, "subject" and "activity". 
8) Write the cleanedData out to "merged_data.txt" file in current working directory 
and generate a second independent tidy data set with the average of each measurement for each activity and each subject.

9_ Write the result out to "tidyData.txt" file in current working directory.