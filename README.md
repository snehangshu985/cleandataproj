
#data sets containe activity in Y(six activity), subject (total 30 person in subject)
divided in two sets train and test (0.70 and 0.30 ratio) and 561 experiments features in X (test and train)

First thing done is 
- reading test activities from y (train and test) then merge with rbind in "full_activity"

- reading test subject from subject_train and subject_test then merge with rbind "full_subject"

- reading features i.e. X_test.txt and X_train.txt and merge  "full_features"

- Descriptively change the column names in full_activity from "v1" to "Activity"

- Descriptively change the column names in full_subject from "v1" to "Subject"

- Add names of 561 experiment extracting names from "feature.txt" and add colnames in full_feature 

- It can be seen that activities are numeric in data set i.e. 1, 2, ...6. they need descriptive
- read lables from activity_labes.txt

#FINAL STEP 1
- merge full_features, full_subject, full_activity through cbind
###the above step completed step 1
#FINAL STEP 3 (Uses descriptive activity names to name the activities in the data set)
- Now cange activiy descriptively by factorise it with level as numerirc from activity_labels$V1
	and label as activity_labels$V2 (which is character)

# FINAL STEP 2 (I complete this step later after step 2, these steps are indipendant)
extract only mean and std dev value with dplyr function 

-  select(contains(c("mean","std", "Activity","Subject")


#Step 4
 variable names changed with gsub(), t as time and f as frequency for every 561 variable

 # STEP 5
again though dplyr - group_by(Activity, Subject) - and  summarise(across(everything(),list(mean))) 

Write this as tidydataset.txt

Thanking you
Regards
Snehangshu Roy