---
title: "Recurrence Data Analysis"
author: "Tom Sanders"
date: "Wednesday, April 06, 2016"
output: html_document
---

```
## Error in setwd("C:/Users/tjs/Google Drive/Breast Center/Recurrence"): cannot change working directory
```
##Summary of Recurrence Data##  
All patients in the Recurrence Database have satisfy the following:  
    
1. Female with a breast cancer  
    a. First occurrence after 1999  
    b. Not soley DCIS  
    c. Not metastitic  
    d. Recurrence not contralateral  
     
2. Known first occurrance values of
    a. ER  
    b. PR  
    c. Number of positive lympth nodes  
    d. Histological Grade  
    e. Tumor size  


```r
summary(data)
```

```
##       ID1              initial.ER       initial.PR     Yrs.to.Recurrence
##  Min.   :      2.0   Min.   :  0.00   Min.   :  0.00   Min.   :0.000    
##  1st Qu.:    133.5   1st Qu.:  0.00   1st Qu.:  0.00   1st Qu.:2.000    
##  Median :    205.0   Median : 80.00   Median :  4.00   Median :3.000    
##  Mean   : 190252.9   Mean   : 51.84   Mean   : 26.87   Mean   :3.135    
##  3rd Qu.:    339.0   3rd Qu.: 90.00   3rd Qu.: 61.50   3rd Qu.:4.000    
##  Max.   :1048696.0   Max.   :100.00   Max.   :100.00   Max.   :9.000    
##  RecurrTime_years TumorSizeSurg    HistGradeSurg  PosNodesSurg   
##  Min.   :0.250    Min.   : 0.030   I  :18        Min.   : 0.000  
##  1st Qu.:1.580    1st Qu.: 1.500   II :63        1st Qu.: 0.000  
##  Median :2.670    Median : 2.400   III:90        Median : 2.000  
##  Mean   :3.236    Mean   : 2.756                 Mean   : 3.754  
##  3rd Qu.:4.460    3rd Qu.: 3.450                 3rd Qu.: 5.000  
##  Max.   :9.500    Max.   :18.000                 Max.   :28.000
```
###First 6 rows of Recurrence Data###  

```
##   ID1 initial.ER initial.PR Yrs.to.Recurrence RecurrTime_years
## 1   2         96          0                 3             3.50
## 2   4         90         70                 6             5.67
## 3   7         90          0                 1             1.08
## 4   8          0          0                 3             3.08
## 5  10          0         50                 2             2.08
## 6  12          0          0                 2             1.83
##   TumorSizeSurg HistGradeSurg PosNodesSurg
## 1          0.35             I            0
## 2          2.50            II            2
## 3          5.00            II            1
## 4          3.00           III            5
## 5          0.50           III            0
## 6          3.70           III            0
```
###Number of Patients: ###

```
## [1] 171
```


###Number of Positive Nodes:###   

![plot of chunk numbPosNode](figure/numbPosNode-1.png)

```
## (-0.1,0]    (0,3] (3,28.1] 
##       57       55       59
```
Do we want to look at other groupings?

###Histological Grade###  

![plot of chunk histGrade](figure/histGrade-1.png)

```
##   I  II III 
##  18  63  90
```
Appears Grade III has a shorter time to recurrence than I-II.  
  
###ER Groups###

![plot of chunk ERgroups](figure/ERgroups-1.png)

```
## (-0.1,10]   (10,79]  (79,100] 
##        69        16        86
```
Alternate Grouping since 11-79 and 80-100 cross.  

![plot of chunk ERgroup2](figure/ERgroup2-1.png)

```
## (-0.1,10]  (10,100] 
##        69       102
```
Appears that ER 0-10 has a shorter recurrence time than 11-100.  
  
  
###PR Groups###
![plot of chunk PRgroups](figure/PRgroups-1.png)

```
##  (-1,0] (0,100] 
##      83      88
```
Appears that PR 0 has shorter recurrence time than 1-100.  
  
  
###Data Summary for 0 Positive Nodes###


```
##       ID1            initial.ER       initial.PR     Yrs.to.Recurrence
##  Min.   :      2   Min.   :  0.00   Min.   :  0.00   Min.   :0.000    
##  1st Qu.:    145   1st Qu.:  0.00   1st Qu.:  0.00   1st Qu.:2.000    
##  Median :    268   Median : 75.00   Median :  0.00   Median :3.000    
##  Mean   : 257705   Mean   : 47.46   Mean   : 24.67   Mean   :3.316    
##  3rd Qu.:    366   3rd Qu.: 90.00   3rd Qu.: 60.00   3rd Qu.:4.000    
##  Max.   :1048694   Max.   :100.00   Max.   :100.00   Max.   :8.000    
##  RecurrTime_years TumorSizeSurg   HistGradeSurg  PosNodesSurg
##  Min.   :0.250    Min.   :0.300   I  : 8        Min.   :0    
##  1st Qu.:2.080    1st Qu.:1.000   II :17        1st Qu.:0    
##  Median :3.000    Median :1.500   III:32        Median :0    
##  Mean   :3.509    Mean   :1.829                 Mean   :0    
##  3rd Qu.:4.920    3rd Qu.:2.500                 3rd Qu.:0    
##  Max.   :8.420    Max.   :8.300                 Max.   :0
```

###ER Survival Curves for 0 Positive Nodes###  

<h4>ER Groups 0-10, 11-79, 80-100 with 0 Positive Nodes</h4>  
![plot of chunk ER0Group1](figure/ER0Group1-1.png)

```
##  (-1,10]  (10,79] (79,100] 
##       27        2       28
```
With only 2 patients in the 11-79 group, I decided to look at some different groupings

<h4>ER groups 0-10, 11-100</h4>
![plot of chunk ER0group2](figure/ER0group2-1.png)

```
##  (-1,10] (10,100] 
##       27       30
```

<h4>ER Groups 0, 1-79, 80-100</h4>
![plot of chunk ER0group3](figure/ER0group3-1.png)

```
##   (-1,0]   (0,79] (79,100] 
##       17       12       28
```

<h4>ER Groups 0, 1-100</h4>
![plot of chunk ER0group4](figure/ER0group4-1.png)

```
##  (-1,0] (0,100] 
##      17      40
```

###PR for 0 Positive Nodes###
![plot of chunk PR0](figure/PR0-1.png)

```
##  (-1,0] (0,100] 
##      29      28
```
