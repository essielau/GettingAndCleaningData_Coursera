This document explains the variables, the data, and transformations that I have done when clean up the data.

•	Download the data for the project:
https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

•	The run_analysis.R script performs the following steps to clean the data:

a)	Store X_train.txt, y_train.txt and subject_train.txt in trainData, trainLabeland trainSubject variables respectively.

b)	Store X_test.txt, y_test.txt and subject_test.txt in testData, testLabel andtestsubject variables respectively.

c)	Concatenate testData to trainData to generate a 10299x561 data frame, joinData; concatenate testLabel totrainLabel to generate a 10299x1 data frame, joinLabel; concatenate testSubject to trainSubject to generate a 10299x1 data frame, joinSubject.

d)	Read and store the features.txt file from the "/data" folder in a variable called features. We extract the measurements on the mean and standard deviation, so we get a subset of joinDatawith the 66 corresponding columns.

e)	Clean the column names of the subset.

f)	Read and store the activity_labels.txt file from the "./data" folder in a variable called activity.

g)	Clean the activity names in the second column of activity. 

h)	Transform the values of joinLabel according to the activity data frame.

i)	Combine the joinSubject, joinLabel and joinData by column to get a new cleaned data frame,cleanedData.

j)	Output the cleanedData to "merged_data.txt" file in current working directory.

k)	Generate a second independent tidy data set with the average of each measurement for each activity and each subject. We have 30 unique subjects and 6 unique activities, which result in a 180 combinations of the two. Calculate the mean of each measurement with the corresponding combination. Therefore, after initializing the result data frame and performing the two for-loops, we get a 180x68 data frame.

l)	Output the result to "data_with_means.txt" file in current working directory.

