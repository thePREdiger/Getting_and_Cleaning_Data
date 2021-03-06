# CodeBook Class

Basis Dataset
https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip
See the README.md for instructions to run the analysis.


The R script *run_analysis.R* contains the following transformations:

* Merges the training and test sets to create one dataset 
  * X_train.txt & X_test.txt
  * Y_train.txt & Y_test.txt
  * subject_train.txt & subject_test.txt

* Based on the *features.txt* file, only measurements on the mean and standard deviation are extracted
  * all features with the strings *mean* and *std* in their name are used

* Use labels based on *activity_labels.txt* and apply. Labels in use are: 
  * walking
  * walkingupstairs
  * walkingdownstairs
  * sitting
  * standing
  * laying

* Labels are streamlined
  * lowercase
  * underscores are removed

* The result is saved as *merged_clean_data.txt*
  * 10299 rows of data
  * 68 columns (subjectID, activity name, 66 measurements)

* A second result is saved as *tidy_data_set.txt* holding the averages of each measurement based on the activity per subject
  * 180 rows of data
  * 68 columns (subjectID, activity name, 66 measurements)