# My First Awesome Project - Bike Share

This is my first project in R, used to identify differences in bike usage between casual riders and annual members to create a marketing plan that converts casual riders into annual members.


## 🤔 Why?

The structured steps (Ask, Prepare, Process, Analyze, Share, Act) are essential because the two datasets (2019_Q1 and 2020_Q1) are inconsistent in format and structure, yet need to be combined to achieve the project's goal.

## 💻 Steps in RStudio
Please take a look at the [.Rmd](https://github.com/Behindpea/bike_share/blob/main/Cyclistic_RMarkdown.Rmd) file to have more detail

* Step 1: Ask - Define the business tasks
This step defined the clear business task: identifying differences between annual members and casual riders to create a conversion strategy. This focus dictates all subsequent data cleaning and analysis.
* Step 2: Prepare - Collect and load data
	- Make sure you have *tidyverse* package installed.
  - In this project, the following datasets will be used [Divvy 2019 Q1](https://docs.google.com/spreadsheets/d/1uCTsHlZLm4L7-ueaSLwDg0ut3BP_V4mKDo2IMpaXrk4/template/preview?resourcekey=0-dQAUjAu2UUCsLEQQt20PDA#gid=1797029090) and [Divvy 2020 Q1](https://docs.google.com/spreadsheets/d/179QVLO_yu5BJEKFVZShsKag74ZaUYIF6FevLYzs3hRc/template/preview#gid=640449855)
* Step 3: Process - Wrangle data and clean
	- Column names of the two datasets aren't the same, we need to make them consistent (E.g., ended_at in dataset 2029 corresponds to end_time in dataset 2020)
  -  Convert data type
	-  Merge data
	-  Remove the redundant columns (like gender, birthyear, etc., they don't contribute to the analysis)
	-  Change q1_2019 user types ('Subscriber', 'Customer') to the q1_2020 format ('member', 'casual')
	-  Create a new column 'ride_length'
	-  Create date/time components for analysis
	-  Filter out negative/zero-length rides and rides longer than 24 hours (extreme outliers)
	-  Drop any rows with missing station names
* Step 4: Analyze - Aggregate and Summarize
This step directly answered the "how do they use bikes differently" question.
	-  Overall Summary Statistics
  -  Analyze usage by days of the week
	-  Analyze usage by month
	-  Identify the top 10 starting stations for each user type
* Step 5: Share - Visualizing data
	-  Compare total rides by days of the week
  -  Average ride length by day of week
* Step 6: Act - Formulate recommendations
The data allows us to recommend highly geo-targeted campaigns (e.g., at Shedd Aquarium) and time-of-day marketing because the user profiles were so clearly distinct.

## 🚀 Report in HTML format

In case you want to view this project report in HTML format, you can also download the [.html](https://github.com/Behindpea/bike_share/blob/main/Cyclistic_RMarkdown.html) file.
