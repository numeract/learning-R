# Data Wrangling Exercise: Human Activity Recognition


## Descriptions

In real life there are many case where the requirements are not very clear or the data is provided in an format different from what we intend to use. This exercise is half away between nice course exercises and real life projects.

Goals: load, merge, extract, transform the dataset to a tidy data format. To show competency, consider using only `tidyverse` functions for all these operations. If you need to make assumptions in order to proceed, please state these assumptions in your code comments.

This exercise based on the course project in [Getting and Cleaning Data](https://www.coursera.org/learn/data-cleaning) course at Coursera.


## Data Set

Human Activity Recognition database built from the recordings of 30 subjects performing activities of daily living while carrying a waist-mounted smartphone with embedded inertial sensors. Please find more details here:

http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

Reference: Davide Anguita, Alessandro Ghio, Luca Oneto, Xavier Parra and Jorge L. Reyes-Ortiz. A Public Domain Dataset for Human Activity Recognition Using Smartphones. 21th European Symposium on Artificial Neural Networks, Computational Intelligence and Machine Learning, ESANN 2013. Bruges, Belgium 24-26 April 2013.

Data link: http://archive.ics.uci.edu/ml/machine-learning-databases/00240/


## Assignment

1: Load the data, ignore Inertial Signals

2: Merge data sets (train, test and X, y, subject, labels, etc.) into one data frame

3. Create variables called `ActivityLabel` and `ActivityName` that label all observations with the corresponding activity labels and names respectively
    + optional, consider renaming the columns such that the names follow the style guide

4: Transform: add two columns containing the mean and standard deviation for each observation.

5: Create tidy data set selecting only the mean and std features (columns) for each measurement. Hint: inspect the names (and read the doc) to see the pattern. 

6. From the data set in step 5, creates a summary tidy data set containing the average of each column for each activity and each subject. 


## Submit

1. The R code for the above
2. The tidy data set from step 5
3. A [data dictionary](https://www.sqlshack.com/sql-server-data-dictionary-want-create-one/) / "code book" that describes the variables, the data, and any transformations performed (consider using a Markdown .md file)

