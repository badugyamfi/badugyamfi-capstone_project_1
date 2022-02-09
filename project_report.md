# Case Study: How Does a Bike-Share Navigate Speedy Success?
![Capture](https://user-images.githubusercontent.com/98782609/152880971-c961c005-6dfa-4583-be25-11560b59982a.JPG)


## Introduction

This report captures the steps, tools and codes used to analyze dataset from Cyclistic to reveal some insights into the data that can be used by stakeholders to meet their objectives.
The main objective of this project is to **Design marketing strategies aimed at converting casual riders into annual members**.

The detail case study can be found [here](https://www.coursera.org/learn/google-data-analytics-capstone/supplement/7PGIT/case-study-1-how-does-a-bike-share-navigate-speedy-success) at the **Google Data Analytics Professional Certificate** course or at this [Link.](https://d18ky98rnyall9.cloudfront.net/aacF81H_TsWnBfNR_x7FIg_36299b28fa0c4a5aba836111daad12f1_DAC8-Case-Study-1.pdf?Expires=1644364800&Signature=R56OjAyx9ZGBJPJEBLihJv0~vicHKxREKbY8K5iqEt1-Pf36-7oCE24uREWPN6SuLSp6rtKH66zK7BNZYUPj02wTf-RMP8byTma0yubDh~8-mtozlvCU5kQVDLZfQTHBb-5jn3qJCf5TF0iofrqTWar5iI39U10qWEzerJ7ehLg_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

The dataset used for this study can be found at this [Link.](https://divvy-tripdata.s3.amazonaws.com/index.html) The data has been made available by
Motivate International Inc. under this [License.](https://ride.divvybikes.com/data-license-agreement)


As a Data Analyst I followed the data analysis step to complete this project:

**ASK**

**PREPARE**

**PROCESS**

**ANALYZE**

**SHARE**

**ACT**




## **ASK**
In the ASK phase, the following questions are considered to help guide the data analyst in this study
1. How do annual members and casual riders use Cyclistic bikes differently?
2. Why would casual riders buy Cyclistic annual memberships?
3. How can Cyclistic use digital media to influence casual riders to become members?

However, this study aims at finding the solution to the first question **How do annual members and casual riders use Cyclistic bikes differently?**

I began with considering the following question:
-  What is the problem you are trying to solve?

The main objective for the marketing department is to **Design marketing strategies aimed at converting casual riders into annual members**.

-  How can your insights drive business decisions?

The insight to this dataset will be used to design marketing strategies to increse the number of annual members.




## **PREPARE**

The dataset used for this study can be found at this [Link.](https://divvy-tripdata.s3.amazonaws.com/index.html) 

The data has been made available by Motivate International Inc. under this [License.](https://ride.divvybikes.com/data-license-agreement)

The tools I used in this phase are: Excel and SQL.

The original dataset is compiled on a monthly basis. I downloaded dataset from the above link, renamed, and uploaded into SQL for further manipulation.



## **PROCESS**

This step covers the steps taken to process the data to get it ready for the analysis and visualization.

The original data was in csv file format. And there were initially 21 files with monthly Cyclistic trip data starting from 2020-04 to 2021-12.

Each of the files were uploaded to postgreSQL for cleaning.

The data cleaning codes used are found in the [bike_share](bike_share.ipynb) notebook.

The steps in the above jupyter notebook are summarized as follows:

- First, all the data was uploaded directly to PostgreSQL.
- Set up the conda environment and opened the jupyter notebook
- Combined all the 21 different data into a single file and eliminated duplicate using the **UNION** command
- Eliminated all rows with null values
- Eliminated all row whose start date is after the end data
- Extracted the last 12 months of data for the study



## **ANALYZE**

This phase covers the steps used to analyze the cleaned data. In this phase I used Tableau. As the data was already cleaned, it did not need any further cleaning.

However, various calculated fields were created to help with the analysis. These include:
- Ride Duration (hours) code: DATEDIFF('hour',[Started At],[Ended At],'sunday')
- Ride Duration (minutes) code: DATEDIFF('minute',[Started At],[Ended At],'sunday')
- Day of week code: DATENAME('weekday',[Started At])

Below is a screenshot of the Tableau dashboard created for this project.
![image](https://user-images.githubusercontent.com/98782609/153142026-61f5611c-1068-46ff-a439-5ba487e5543d.png)
The work done in Tableau can be accessed at this Tableau Public [Link.](https://public.tableau.com/views/Capstone_project_1_16443091886810/Cyclistic2021?:language=en-US&:display_count=n&:origin=viz_share_link)



The general overview of the data indicates that there were 10.72% more many of rides completed by annual members than the casual riders.
![image](https://user-images.githubusercontent.com/98782609/153013795-1cc5df46-935e-4e9f-8edc-9f29ec55a442.png)



However, further analysis indicates that casual riders accounted for more total and average ride duration than the annual members.
![image](https://user-images.githubusercontent.com/98782609/153016409-27ecd45c-e68f-46bb-8e5e-be52cc0c2761.png)



The total monthly ride duration, expressed in hours, spanning from Jan 2021 to Dec 2021 is displayed as follows.
![image](https://user-images.githubusercontent.com/98782609/153146451-d257c674-be7a-4532-bf53-0ab5455d9b6c.png)



Detailed look at data at weekly and daily level are shown below.
![image](https://user-images.githubusercontent.com/98782609/153153478-b06d6668-f063-48d5-af24-4602ae406095.png)



The are monthly ride duration covered the various bike types; classic, docked, and electric.
![image](https://user-images.githubusercontent.com/98782609/153155126-37709656-40ed-4587-8988-f04b74441920.png)
![image](https://user-images.githubusercontent.com/98782609/153155362-32097561-6efb-478a-bf87-a3442261f8e9.png)
![image](https://user-images.githubusercontent.com/98782609/153155473-16e37e62-e17e-40d1-84cc-5c310b3c4cdd.png)













