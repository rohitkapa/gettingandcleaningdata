# gettingandcleaningdata
This repo consists of assignment solutions for getting and cleaning data course

The below script is written to create a tiny cleaned data set obtained by preprocessing a UCI HAR dataset.
The data set consists of two datasets-train and test each in separate folder.
Check whether the working directory has required dataset or not and if the data set is not present, set the working directory.

Read the 'features.txt' and 'activity_labels.txt' having the description of labels for different features of measurement taken and activities performed by subjects.

Navigate to train data folder and load the 'X_train.txt','y_train.txt','subject_train.txt'.Each of this files has observations for different readings and their corresponding activity and subject labels in the remaining texts. The same is with test data folder.

Combine the two data sets by using rbind() to merge them on a row basis
Labelling the data set with descriptive variable names using the help of data present in features.txt file.


Separate the columns having data related to mean() and std(), this has been acheived by searching for these patterns in column names of the finaldataset.

Add the corresponding values of activities and subject details to our final data set.

Adding the column names to the newly added subject and activity data

Change the activities performed with meaningful convention by changing the data to descriptive activity names, the data related to this can be found from 'activities_label.txt' file.

Factorize the data sothat it will be easy for performing grouping functions.


Finding the mean of all individual rows using dplyr package for each activity_label and subject values

Writing the output of the above data to a tidydataset. The final dataset 'tinydataset' consists of total 68 columns of which first two are activity and subject related data and rest 66 are meaan() and std() related columns with 180 observations grouped by each activity and subject.

Use the read.table() function to read this dataset.

