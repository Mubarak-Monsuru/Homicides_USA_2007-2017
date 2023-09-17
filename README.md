# Homicides_USA_2007-2017

## 1. Purpose of Study
* Conduct detailed analysis on a dataset of recorded homicies in the United States between 2007 and 2017.
* Develop visulaizations to reveal insghts from analysis, such as, homicide and arrest rates between 2007 and 2017, homicide and arrest rates per city, victim demographics etc.

## 2. Dataset
A public dataset published by 'Joakim Arvidsson' on Kaggle <https://kaggle.com/datasets/joebeachcapital/homicides>

## 3.Data Cleaning & Processing
### 3.1 Tool
* MS Excel

### 3.2 Data Cleaning
* Check for duplicates. Dataset does not contain duplicate rows
* change columns 'lat' and 'lon' to 'latitude' and 'longitude' respectively.
* Explore columns to identify blank cells, inappropriate values.
* 2 columns (latitude and longitude) contain blank cells. 3 columns (victim_race, victim_age and victim_sex) contain cells with value 'unknown'
* Remove rows that contain blanks cells and 'unknown'. This reduced number of rows from 52179 to 43397.

### 3.3 Data Processing
* Extract 3 columns (year, month, date)  from column 'reported_date' in custom format. Formula: =LEFT([@[reported_date]];4); =MID([@[reported_date]];5;2); =RIGHT([@[reported_date]];2).
* Create a new column for 'reported_date'. Formula: =DATE([@year];[@month];[@date]).
* Change columns 'victim_first' and 'victim_last' to 'first_name' and 'last_name'. Change case of values in both columns to proper case. Formula: =PROPER([@[last_name]]); =PROPER([@[first_name]]).
* Create a new column 'age_demographic' from column 'victim_age' to categorise victims by age groups. Formula: =IF(J2<=12;"Child";IF(J2<=17;"Adolescent";IF(J2<=65;"Adult";"Old"))).

## 4. Results

### 4.1
![image](https://github.com/Mubarak-Monsuru/Homicides_USA_2007-2017/assets/141940008/604d7b68-a615-461f-9be4-bf412c340481)

The analyis of homicide data spanning from 2007 to 2017 reveals an upward trend in the rate of homicides, and there is a significant drop in arrest rates during the same time period. In 2007, over 50% of homicide cases resulted in arrests, but by 2017, arrest percentage had plummeted to less than 40%.

### 4.2
![image](https://github.com/Mubarak-Monsuru/Homicides_USA_2007-2017/assets/141940008/4a73a737-e3ba-45ae-9158-f9f89fc0083e)

The above chart unveils recorded homicide cases in U.S. cities and their corresponding arrest rates. The result shows glaring disparities in law enforcement outcomes and these cities exhibit varying levels of safety and justice.

### 4.3
![image](https://github.com/Mubarak-Monsuru/Homicides_USA_2007-2017/assets/141940008/044580e7-3365-4bf7-84b4-7bcf6fef7377)

The analysis reveals 72% of victims being black and a quarter of victims being either White or Hispanic. This accentuates the urgent need for government and law enforcement agencies to introduce more safety initiaves in predominantly black neighborhoods.

#### 4.4
![image](https://github.com/Mubarak-Monsuru/Homicides_USA_2007-2017/assets/141940008/59e000c1-eab9-45ec-ac45-e24527672982)

Most homicide victims between 2007 and 2017 were individuals between the age of 18 and 65, classified as adults. This raises significant concerns due to its potential direct impact on the economy when adults are being murdered. The loss of individuals in their working years not only has profound social and emotional repercussions but also leads to significant economic burden. It limits the potential workforce, productivity, and future contributions to the economy. Addressing the root causes of violence affecting this age group is not just a matter of public safety but also a critical economic imperative for communities and policymakers.
