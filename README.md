READ ME
==============

###Prerequisites

**sqldf** package must be installed.

###Running script

Before running the script be sure to change the three global variables if they does not match your environment. 

```R
## Path to data folder or path inside working folder
datapath <- "UCI HAR Dataset"

## Path separator, "\\" for Windows, "/" for Unix
pathSeparator <- "\\"

## Output file name (CSV format)
outputFile <- "tidydata.txt"
```

The script first check if there is a folder with the dataset. If there is none, the zip file is downloaded and unzipped.

The run_analysis function first loads the train data set, then loads the test data set and then binds them together. Then it uses the sqldf to proccess the data and finally it writes a CSV file with the tidy data set. This file has ".txt" extension instead of ".csv" because Coursera does not allow to upload CSV files in the assignment page.

###IMPORTANT NOTE

The output file will be rewritten without prompt.