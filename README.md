# Course_Project
Repository with information of course project from Getting and Cleaning data course (Coursera)

## How to create a tidy data
Here you have all the information to do the tidy data uploaded.

### 1) Create a file where the data will be downloaded, download and unzip the data.
if(!file.exists("Course_Project")) {dir.create("Course_Project")}

fileUrl <- "https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip"

download.file(fileUrl, destfile="./Course_Project.zip")

unzip("Course_Project.zip")

### 2) Read all the files, using read.table function and merge them.
First, read files in the main directory (UCI_HAR_Dataset): features.txt and activity_labels.txt.
For features file, eliminate the first column, since only the second column will be used to name the columns of the merged data.

features <- read.table("./UCI_HAR_Dataset/features.txt", header=FALSE, sep="", colClasses="character", na.strings="NA")

features <- features[,2]

activity_labels <- read.table("./UCI_HAR_Dataset/activity_labels.txt", header=FALSE, sep="", colClasses="character", na.strings="NA")


After, read files for each directory inside the main directory, in which contain infomation from test and train values.
After you read all files inside test directory, merge them in one data set named "test". Use "feature" to give names for the columns.

x_test <- read.table("./UCI_HAR_Dataset/test/X_test.txt", header=FALSE, sep="", colClasses="numeric", na.strings="NA")

y_test <- read.table("./UCI_HAR_Dataset/test/y_test.txt", header=FALSE, sep="", colClasses="factor", na.strings="NA")

subject_test <- read.table("./UCI_HAR_Dataset/test/subject_test.txt", header=FALSE, sep="", colClasses="numeric", na.strings="NA")

test <- cbind(subject_test,y_test,x_test)

colnames(test) <- c("subject", "activity", features)


Do the same for the files in train directory, creating a data set named "train"

x_train <- read.table("./UCI_HAR_Dataset/train/X_train.txt", header=FALSE, sep="", colClasses="numeric", na.strings="NA")

y_train <- read.table("./UCI_HAR_Dataset/train/y_train.txt", header=FALSE, sep="", colClasses="factor", na.strings="NA")

subject_train <- read.table("./UCI_HAR_Dataset/train/subject_train.txt", header=FALSE, sep="", colClasses="numeric", na.strings="NA")

train <- cbind(subject_train,y_train,x_train)

colnames(train) <- c("subject", "activity", features)


Finally, merge data sets test and train in one big data set named "data_set", using rbind (you have two data sets with the same columns, but different number of rows).

data_set <- rbind (test, train)

### 3) Create a new dataset contaning only information of interested columns.
Select columns that contain information of mean and standard deviation for each measurement. For this, use grep, and select columns by the name (containing "mean()" or "std()" in the name).

data_set2 <- data_set[, c(1,2,as.vector(grep("mean()|std()", names(data_set))))] 


Using the selection above, some unwelcome variables that contain "mean" in the name were selected. To exclude this columns, extracts them using grep again.

data_set2 <- data_set2[,-(as.vector(grep("meanFreq", names(data_set2))))]

### 4) Use descriptive activity names to name the activities in the data set.
For this, use the mapvalues from the plyr package.

Install.packages("plyr")

library(plyr)

data_set2$activity <- mapvalues(data_set2$activity, from=c("1","2","3","4","5","6"), to = c("walking", "walking_upstairs", "walking_downstairs", "sitting", "standing", "laying"))

### 5) Appropriately label the data set with descriptive variable names.
colnames(data_set2) <- c("subject", "activity", "tBodyAccMeanX", "tBodyAccMeanY", "tBodyAccMeanZ", "tBodyAccStdX", "tBodyAccStdY", "tBodyAccStdZ", "tGravityAccMeanX", "tGravityAccMeanY",
           "tGravityAccMeanZ", "tGravityAccStdX", "tGravityAccStdY", "tGravityAccStdZ", "tBodyAccJerkMeanX",  "tBodyAccJerkMeanY", "tBodyAccJerkMeanZ",
           "tBodyAccJerkStdX", "tBodyAccJerkStdY", "tBodyAccJerkStdZ", "tBodyGyroMeanX", "tBodyGyroMeanY", "tBodyGyroMeanZ", "tBodyGyroStdX",
           "tBodyGyroStdY", "tBodyGyroStdZ", "tBodyGyroJerkMeanX", "tBodyGyroJerkMeanY", "tBodyGyroJerkMeanZ", "tBodyGyroJerkStdX",
           "tBodyGyroJerkStdY", "tBodyGyroJerkStdZ", "tBodyAccMagMean", "tBodyAccMagStd", "tGravityAccMagMean", "tGravityAccMagStd",
           "tBodyAccJerkMagMean", "tBodyAccJerkMagStd", "tBodyGyroMagMean", "tBodyGyroMagStd", "tBodyGyroJerkMagMean", "tBodyGyroJerkMagStd",
           "fBodyAccMeanX", "fBodyAccMeanY", "fBodyAccMeanZ", "fBodyAccStdX", "fBodyAccStdY", "fBodyAccStdZ", "fBodyAccJerkMeanX", "fBodyAccJerkMeanY",
           "fBodyAccJerkMeanZ", "fBodyAccJerkStdX", "fBodyAccJerkStdY", "fBodyAccJerkStdZ", "fBodyGyroMeanX", "fBodyGyroMeanY", "fBodyGyroMeanZ",
           "fBodyGyroStdX", "fBodyGyroStdY", "fBodyGyroStdZ", "fBodyAccMagMean", "fBodyAccMagStd", "fBodyBodyAccJerkMagMean", "fBodyBodyAccJerkMagStd",
           "fBodyBodyGyroMagMean", "fBodyBodyGyroMagStd", "fBodyBodyGyroJerkMagMean", "fBodyBodyGyroJerkMagStd")

### 6) Create a second, independent tidy data set with the average of each variable for each activity and each subject.
For this, use group_by and summarise_each form dplyr packages.

Install.packages("dplyr")

library(dplyr)

tidy <- data_set2 %>% group_by (activity, subject) %>% summarise_each(funs(mean))

### 7) Save the tidy data using write.table.
write.table (tidy, file="tidy_dataset.txt", sep=" ", dec=".", row.names=FALSE, col.names=TRUE)
