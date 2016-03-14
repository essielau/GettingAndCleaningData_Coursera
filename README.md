This is the project for 'Getting and Cleaning Data' course

To run this project you will need this data: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

Unpack the data as to have 'UCI HAR Dataset' directory and its subdirectories inside your working directory.  
Change the name of the file to data.
Copy run_analysis.R to your working directory.
Install the 'plyr' package if you don't have it.

To reproduce this project:

1. Unzip the data from https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip and rename the folder with "data".
Keep the folder "data" and the run_analysis.R script both in the current working directory.

2. Use source("run_analysis.R") command in RStudio.

3. Two output files will be generated in the current working directory:
merged_data.txt: it contains a data frame called cleanedData with 10299*68 dimension.
data_with_means.txt: it contains a data frame called result with 180*68 dimension.

4. Use data <- read.table("data_with_means.txt") command in RStudio to read the file. There are 6 activities and 30 subjects in total.
