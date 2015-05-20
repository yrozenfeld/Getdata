# Code book

Thisi document describes the code inside run_analysis.R

* Creates data subfolder after checking if this subfodler exists
* Unzips the data set after downloading it from the https://  address
* Reads activity test and train data using read.table statements
* Reads Subject test and train data using read.table statements
* Reads features test and train data using read.table statements
* Combine test and train sets separately for subjets, activities, and features using rbind statement by rows
* Set names to features 
* Merge columns using cbind to bring all data
* Extract all variable with has part of the name mean() and std() using grep statement that looks
 for matches to argument pattern within each element of a char vector
* Read activity categories file using read.table statement
* Factorize activity values by using factor function which encodes a vector as a factor
* Naming using descriptives
* Create tidy data set using plyr package
* Write tidedata.txt file using write.table command
