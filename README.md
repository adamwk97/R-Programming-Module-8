R Programming Module \# 8 assignment
================

First we import the dataset and then create a column for average grades by gender and append it to a new dataframe.

``` r
df <- read.csv("C:/Users/adamw/Downloads/Assignment 6 Dataset-1.txt")

StudentAverage = ddply(df,"Sex",transform,Grade.Average=mean(Grade))
```

Now we can subset the dataframe and only keep rows that have names which contain an "i" and then export the file to a csv.

``` r
i_students = subset(df, grepl("i", df$Name, ignore.case=T))
write.csv(i_students, "i_Students_Gendered_Mean")
```

While I am familiar with the first half of the assignment concerning subsetting and appending new columns of data, I had not really ever exported a dataset so it was interesting and nice to see how simple it is. I was able to load the file into Excel with no problem.

![Screenshot of data in Excel](C:\Users\adamw\Documents\R%20Programming%20Class\Module%208\i-students.png)
