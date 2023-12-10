---
title: "Script Explanation and Code Book"
author: "Serhii"
date: "December 10, 2023"
output: html_document
---

# Script Explanation

This R script performs data preprocessing and manipulation tasks using the UCI Human Activity Recognition Dataset. Here's a breakdown of the script's functionality:

1. **Package Loading and Data Downloading**: Initially, it loads required packages like `data.table` and `reshape2`. Then, it downloads the dataset from a specified URL, unzips it, and sets the working directory.

2. **Loading Activity Labels and Features**: The script reads in activity labels and features from relevant text files. It selects specific features related to mean and standard deviation measurements from the features dataset.

3. **Loading and Processing Train Datasets**: Train datasets are loaded, filtering columns based on the selected features. Activity labels, subject numbers, and data are combined into a single train dataset.

4. **Loading and Processing Test Datasets**: Similar to the train datasets, test datasets are loaded, filtered, and combined into a single test dataset.

5. **Merging Datasets**: Both train and test datasets are merged to create a unified dataset.

6. **Data Transformation**: Class labels are converted to activity names, and SubjectNum is converted to a factor. The dataset is reshaped using the `melt` and `dcast` functions from the `reshape2` package to calculate the mean of each variable for each activity and subject.

7. **Data Export**: Finally, the resulting tidy dataset is exported to a file named "tidyData.txt" using the `write.table` function.

# Code Book

Here's a brief description of the variables present in the resulting tidy dataset:

- **SubjectNum**: Identifies the subject who performed the activity (Factor).
- **Activity**: Descriptive name of the activity performed by the subject (Factor).
- **Other Variables**: Various measurements related to mean and standard deviation calculations for different features in the dataset. These measurements are calculated and aggregated for each subject and activity.

The exact details of the measurements and features can be found in the original dataset documentation provided by UCI Human Activity Recognition Dataset.

Please refer to the script for the full data preprocessing and transformation steps.

