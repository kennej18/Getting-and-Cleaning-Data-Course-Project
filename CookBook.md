#Introduction 
The script run_analysis.R performs the 5 steps described in the course project's definition.
•	Merges training and the test set to create one data set using the rbind() function. Using same number of columns and referring to the same entities provided.
•	Then, mean and standard deviation measures are taken from the whole dataset, and extracting these columns, and made name correction from features.txt.
•	We take the activity names and IDs from activity_labels.txt and they are substituted in the dataset. On the whole dataset, those columns with vague column names are corrected.
•	Finally, we generate a new dataset with all the average measures for each subject and activity type (30 subjects * 6 activities = 180 rows). The output file is called tidy_data.txt, and uploaded to this repository.
Variables
•	x_train, y_train, x_test, y_test, subject_train and subject_test contain the data from the downloaded files.
•	x_data, y_data and subject_data merge the previous datasets to further analysis.
•	features contains the correct names for the x_data dataset, which are applied to the column names stored in mean_and_std_features, a numeric vector used to extract the desired data.
•	A similar approach is taken with activity names through the activities variable.
•	comb_data merges x_data, y_data and subject_data in a big dataset.
•	Finally, tidy_data contains the relevant averages which will be later stored in a .txt file. ddply() from the plyr package is used to apply colMeans() and ease the development.

