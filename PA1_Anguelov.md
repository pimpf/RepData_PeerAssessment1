# Reproducible Research: Peer Assessment 1


## Loading and preprocessing the data
Let first load libraries which I will be using and load the data from the given file. It is zipped. So first check if it is already unzipped *(file exists)* and the read it using **read.csv** function.

```r
# import some libraries
library(dplyr)
```

```
## 
## Attaching package: 'dplyr'
## 
## The following object is masked from 'package:stats':
## 
##     filter
## 
## The following objects are masked from 'package:base':
## 
##     intersect, setdiff, setequal, union
```

```r
library(lattice)
library(tidyr)
library(lubridate)

# check if the file was already unzipped
fName <- "activity.csv";

if(!file.exists(fName)){
    unzip("activity.zip", fName);
}

# read the data and store it in activity dataframe
activity <- read.csv("activity.csv", sep = ",", na.strings = "NA");
```
   
Now that we have our data let's take a look at it. For this part we can ignore missing data.

```r
str(activity);
```

```
## 'data.frame':	17568 obs. of  3 variables:
##  $ steps   : int  NA NA NA NA NA NA NA NA NA NA ...
##  $ date    : Factor w/ 61 levels "2012-10-01","2012-10-02",..: 1 1 1 1 1 1 1 1 1 1 ...
##  $ interval: int  0 5 10 15 20 25 30 35 40 45 ...
```

```r
head(activity, 10);
```

```
##    steps       date interval
## 1     NA 2012-10-01        0
## 2     NA 2012-10-01        5
## 3     NA 2012-10-01       10
## 4     NA 2012-10-01       15
## 5     NA 2012-10-01       20
## 6     NA 2012-10-01       25
## 7     NA 2012-10-01       30
## 8     NA 2012-10-01       35
## 9     NA 2012-10-01       40
## 10    NA 2012-10-01       45
```

## What is mean total number of steps taken per day?



## What is the average daily activity pattern?



## Imputing missing values



## Are there differences in activity patterns between weekdays and weekends?
