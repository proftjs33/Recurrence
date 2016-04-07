---
title: "Recurrence Data Analysis"
author: "Tom Sanders"
date: "Wednesday, April 06, 2016"
output: html_document
---

```
## Error in setwd("C:/Users/tjs/Google Drive/Breast Center/Recurrence"): cannot change working directory
```

```
## Warning in file(file, "rt"): cannot open file '20160402 data.csv': No such
## file or directory
```

```
## Error in file(file, "rt"): cannot open the connection
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
## Error in object[[i]]: object of type 'closure' is not subsettable
```
###First 6 rows of Recurrence Data###  

```
##                                                                      
## 1 function (..., list = character(), package = NULL, lib.loc = NULL, 
## 2     verbose = getOption("verbose"), envir = .GlobalEnv)            
## 3 {                                                                  
## 4     fileExt <- function(x) {                                       
## 5         db <- grepl("\\\\.[^.]+\\\\.(gz|bz2|xz)$", x)              
## 6         ans <- sub(".*\\\\.", "", x)
```
###Number of Patients: ###

```
## NULL
```


###Number of Positive Nodes:###   


```
## Error in data$PosNodesSurg: object of type 'closure' is not subsettable
```

```
## Error in Surv(data0$RecurrTime_years): object 'data0' not found
```

```
## Error in summary(data0.surv): object 'data0.surv' not found
```

```
## Error in data$PosNodesSurg: object of type 'closure' is not subsettable
```

```
## Error in Surv(data3$RecurrTime_years): object 'data3' not found
```

```
## Error in summary(data3.surv): object 'data3.surv' not found
```

```
## Error in data$PosNodesSurg: object of type 'closure' is not subsettable
```

```
## Error in Surv(data4$RecurrTime_years): object 'data4' not found
```

```
## Error in summary(data4.surv): object 'data4.surv' not found
```

```
## Error in eval(expr, envir, enclos): object 'surv0' not found
```

```
## Error in eval(expr, envir, enclos): object 'surv3' not found
```

```
## Error in eval(expr, envir, enclos): object 'surv4' not found
```

```
## Error in strwidth(legend, units = "user", cex = cex, font = text.font): plot.new has not been called yet
```

```
## Error in data$PosNodesSurg: object of type 'closure' is not subsettable
```

```
## Error in summary(posNode): object 'posNode' not found
```
Do we want to look at other groupings?

###Histological Grade###  


```
## Error in data$HistGradeSurg: object of type 'closure' is not subsettable
```

```
## Error in Surv(dataI_II$RecurrTime_years): object 'dataI_II' not found
```

```
## Error in summary(dataI_II.surv): object 'dataI_II.surv' not found
```

```
## Error in eval(expr, envir, enclos): object 'survI_II' not found
```

```
## Error in data$HistGradeSurg: object of type 'closure' is not subsettable
```

```
## Error in Surv(dataIII$RecurrTime_years): object 'dataIII' not found
```

```
## Error in summary(dataIII.surv): object 'dataIII.surv' not found
```

```
## Error in eval(expr, envir, enclos): object 'survIII' not found
```

```
## Error in strwidth(legend, units = "user", cex = cex, font = text.font): plot.new has not been called yet
```

```
## Error in data$HistGradeSurg: object of type 'closure' is not subsettable
```
Appears Grade III has a shorter time to recurrence than I-II.  
  
###ER Groups###


```
## Error in data$initial.ER: object of type 'closure' is not subsettable
```

```
## Error in Surv(data.ER.0.10$RecurrTime_years): object 'data.ER.0.10' not found
```

```
## Error in summary(data.ER.0.10.surv): object 'data.ER.0.10.surv' not found
```

```
## Error in eval(expr, envir, enclos): object 'surv.ER.0.10' not found
```

```
## Error in data$initial.ER: object of type 'closure' is not subsettable
```

```
## Error in Surv(data.ER.11.70$RecurrTime_years): object 'data.ER.11.70' not found
```

```
## Error in summary(data.ER.11.70.surv): object 'data.ER.11.70.surv' not found
```

```
## Error in eval(expr, envir, enclos): object 'data.ER.11.70.surv' not found
```

```
## Error in data$initial.ER: object of type 'closure' is not subsettable
```

```
## Error in Surv(data.ER.80.100$RecurrTime_years): object 'data.ER.80.100' not found
```

```
## Error in summary(data.ER.80.100.surv): object 'data.ER.80.100.surv' not found
```

```
## Error in eval(expr, envir, enclos): object 'surv.ER.80.100' not found
```

```
## Error in strwidth(legend, units = "user", cex = cex, font = text.font): plot.new has not been called yet
```

```
## Error in data$initial.ER: object of type 'closure' is not subsettable
```

```
## Error in summary(ERgroup): object 'ERgroup' not found
```
Alternate Grouping since 11-79 and 80-100 cross.  


```
## Error in data$initial.ER: object of type 'closure' is not subsettable
```

```
## Error in Surv(data.ER.0.10$RecurrTime_years): object 'data.ER.0.10' not found
```

```
## Error in summary(data.ER.0.10.surv): object 'data.ER.0.10.surv' not found
```

```
## Error in eval(expr, envir, enclos): object 'surv.ER.0.10' not found
```

```
## Error in data$initial.ER: object of type 'closure' is not subsettable
```

```
## Error in Surv(data.ER.11.100$RecurrTime_years): object 'data.ER.11.100' not found
```

```
## Error in summary(data.ER.11.100.surv): object 'data.ER.11.100.surv' not found
```

```
## Error in eval(expr, envir, enclos): object 'surv.ER.11.100' not found
```

```
## Error in strwidth(legend, units = "user", cex = cex, font = text.font): plot.new has not been called yet
```

```
## Error in data$initial.ER: object of type 'closure' is not subsettable
```

```
## Error in summary(ERgroup): object 'ERgroup' not found
```
Appears that ER 0-10 has a shorter recurrence time than 11-100.  
  
  
###PR Groups###

```
## Error in data$initial.PR: object of type 'closure' is not subsettable
```

```
## Error in Surv(data.PR.0$RecurrTime_years): object 'data.PR.0' not found
```

```
## Error in summary(data.PR.0.surv): object 'data.PR.0.surv' not found
```

```
## Error in eval(expr, envir, enclos): object 'surv.PR.0' not found
```

```
## Error in data$initial.PR: object of type 'closure' is not subsettable
```

```
## Error in Surv(data.PR.1.100$RecurrTime_years): object 'data.PR.1.100' not found
```

```
## Error in summary(data.PR.1.100.surv): object 'data.PR.1.100.surv' not found
```

```
## Error in eval(expr, envir, enclos): object 'data.PR.1.100.surv' not found
```

```
## Error in strwidth(legend, units = "user", cex = cex, font = text.font): plot.new has not been called yet
```

```
## Error in data$initial.PR: object of type 'closure' is not subsettable
```

```
## Error in summary(PRgroup): object 'PRgroup' not found
```
Appears that PR 0 has shorter recurrence time than 1-100.  
  
  
###Data Summary for 0 Positive Nodes###


```
## Error in data$PosNodesSurg: object of type 'closure' is not subsettable
```

```
## Error in summary(data0): object 'data0' not found
```

###ER Survival Curves for 0 Positive Nodes###  

<h4>ER Groups 0-10, 11-79, 80-100 with 0 Positive Nodes</h4>  

```
## Error in eval(expr, envir, enclos): object 'data0' not found
```

```
## Error in Surv(data.ER.0.10$RecurrTime_years): object 'data.ER.0.10' not found
```

```
## Error in summary(data.ER.0.10.surv): object 'data.ER.0.10.surv' not found
```

```
## Error in eval(expr, envir, enclos): object 'surv.ER.0.10' not found
```

```
## Error in eval(expr, envir, enclos): object 'data0' not found
```

```
## Error in Surv(data.ER.11.79$RecurrTime_years): object 'data.ER.11.79' not found
```

```
## Error in summary(data.ER.11.79.surv): object 'data.ER.11.79.surv' not found
```

```
## Error in eval(expr, envir, enclos): object 'data.ER.11.79.surv' not found
```

```
## Error in eval(expr, envir, enclos): object 'data0' not found
```

```
## Error in Surv(data.ER.80.100$RecurrTime_years): object 'data.ER.80.100' not found
```

```
## Error in summary(data.ER.80.100.surv): object 'data.ER.80.100.surv' not found
```

```
## Error in eval(expr, envir, enclos): object 'surv.ER.80.100' not found
```

```
## Error in strwidth(legend, units = "user", cex = cex, font = text.font): plot.new has not been called yet
```

```
## Error in cut(data0$initial.ER, c(-1, 10, 79, 100.1)): object 'data0' not found
```

```
## Error in summary(ER0group1): object 'ER0group1' not found
```
With only 2 patients in the 11-79 group, I decided to look at some different groupings

<h4>ER groups 0-10, 11-100</h4>

```
## Error in eval(expr, envir, enclos): object 'data0' not found
```

```
## Error in Surv(data.ER.11.100$RecurrTime_years): object 'data.ER.11.100' not found
```

```
## Error in summary(data.ER.11.100.surv): object 'data.ER.11.100.surv' not found
```

```
## Error in eval(expr, envir, enclos): object 'surv.ER.0.10' not found
```

```
## Error in eval(expr, envir, enclos): object 'surv.ER.11.100' not found
```

```
## Error in strwidth(legend, units = "user", cex = cex, font = text.font): plot.new has not been called yet
```

```
## Error in cut(data0$initial.ER, c(-1, 10, 100.1)): object 'data0' not found
```

```
## Error in summary(ER0group2): object 'ER0group2' not found
```

<h4>ER Groups 0, 1-79, 80-100</h4>

```
## Error in eval(expr, envir, enclos): object 'data0' not found
```

```
## Error in Surv(data.ER.0$RecurrTime_years): object 'data.ER.0' not found
```

```
## Error in summary(data.ER.0.surv): object 'data.ER.0.surv' not found
```

```
## Error in eval(expr, envir, enclos): object 'surv.ER.0' not found
```

```
## Error in eval(expr, envir, enclos): object 'data0' not found
```

```
## Error in Surv(data.ER.1.79$RecurrTime_years): object 'data.ER.1.79' not found
```

```
## Error in summary(data.ER.1.79.surv): object 'data.ER.1.79.surv' not found
```

```
## Error in eval(expr, envir, enclos): object 'data.ER.1.79.surv' not found
```

```
## Error in eval(expr, envir, enclos): object 'data0' not found
```

```
## Error in Surv(data.ER.80.100$RecurrTime_years): object 'data.ER.80.100' not found
```

```
## Error in summary(data.ER.80.100.surv): object 'data.ER.80.100.surv' not found
```

```
## Error in eval(expr, envir, enclos): object 'surv.ER.80.100' not found
```

```
## Error in strwidth(legend, units = "user", cex = cex, font = text.font): plot.new has not been called yet
```

```
## Error in cut(data0$initial.ER, c(-1, 0, 79, 100.1)): object 'data0' not found
```

```
## Error in summary(ER0group3): object 'ER0group3' not found
```

<h4>ER Groups 0, 1-100</h4>

```
## Error in eval(expr, envir, enclos): object 'surv.ER.0' not found
```

```
## Error in eval(expr, envir, enclos): object 'data0' not found
```

```
## Error in Surv(data.ER.1.100$RecurrTime_years): object 'data.ER.1.100' not found
```

```
## Error in summary(data.ER.1.100.surv): object 'data.ER.1.100.surv' not found
```

```
## Error in eval(expr, envir, enclos): object 'surv.ER.1.100' not found
```

```
## Error in strwidth(legend, units = "user", cex = cex, font = text.font): plot.new has not been called yet
```

```
## Error in cut(data0$initial.ER, c(-1, 0, 100.1)): object 'data0' not found
```

```
## Error in summary(ER0group4): object 'ER0group4' not found
```

###PR for 0 Positive Nodes###

```
## Error in eval(expr, envir, enclos): object 'data0' not found
```

```
## Error in Surv(data.PR.0$RecurrTime_years): object 'data.PR.0' not found
```

```
## Error in summary(data.PR.0.surv): object 'data.PR.0.surv' not found
```

```
## Error in eval(expr, envir, enclos): object 'surv.PR.0' not found
```

```
## Error in eval(expr, envir, enclos): object 'data0' not found
```

```
## Error in Surv(data.PR.100$RecurrTime_years): object 'data.PR.100' not found
```

```
## Error in summary(data.PR.1.100.surv): object 'data.PR.1.100.surv' not found
```

```
## Error in eval(expr, envir, enclos): object 'surv.PR.100' not found
```

```
## Error in strwidth(legend, units = "user", cex = cex, font = text.font): plot.new has not been called yet
```

```
## Error in cut(data0$initial.PR, c(-1, 0, 100)): object 'data0' not found
```

```
## Error in summary(PR.0): object 'PR.0' not found
```
