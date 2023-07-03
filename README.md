# Google Data Analytics Capstone Project
Case Study: How Does a Bike-Share Navigate Speedy Success?

## Background ##

  In 2016, Cyclistic launched a successful bike-share offering. Since then, the program has grown to a fleet of 5,824 bicycles that are geotracked and locked into a network of 692 stations across Chicago. The bikes can be unlocked from one station and returned to any other station in the system anytime. Until now, Cyclistic’s marketing strategy relied on building general awareness and appealing to broad consumer segments. One approach that helped make these things possible was the flexibility of its pricing plans: single-ride passes, full-day passes, and annual memberships. Customers who purchase single-ride or full-day passes are referred to as casual riders. Customers who purchase annual memberships are Cyclistic members.

## 1. Ask

### Business Question:

How do annual members and casual riders use Cyclistic bikes differently?

Key Stakeholders:

    Lily Moreno
    Cyclistic marketing analytics team
    Cyclistic executive team

### Business Task:

Use the data to explore and gain insights on how annual members and casual riders use bikes differently. From trends and insights, assist the team to implement marketing strategies aimed at converting casual riders into annual members.

## 2. Prepare

The data include information about Cyclistic's historical trip and customers' patterns in bike usage. It is obtained between April 2022 and March 2023 (12 months).

Link: [Data Source] (https://divvy-tripdata.s3.amazonaws.com/index.html)


## 3. Process

I use R language due to its flexibility to process large datasets, and R Studio as main tool to work data more efficiently. Data cleaning, analysis, and visualization will be processed with R.

### Data Preparation

  - Libraries used: *tidyverse, lubridate, ggplot2*
  - Data format: *csv*.  Data granulation: monthly
  - Data columns checked for possible name inconsistencies
  - A single dataframe was compiled using the available data (12 months of the given year)

### Date Cleaning

  - Created support columns (*date, month, day, year* and *day of week*) for deeper dive in the data analysis and removed *start_lat, start_lng, end_lat* and *end_lng* columns from the data as they were not needed.
  - Missing values were dealt using `na.omit()`
  - Generated a new column (ride length) in minutes with `difftime()`
  - Converted the ride length column into numeric
  - Excluded negative or zero ride lengths from data
  - Ordered the day of week column

## 4. Analyze

**"How do annual members and casual riders use Cyclistic bikes differently?"**

The analyze phase will explore the forementioned question by performing a descriptive statistical analysis and aggregating the data with * group by * to extract trends from bike users.

### Descriptive analysis ###

  - Calculated the *mean, median, min* and *max* on *ride length* column
  - For each kind of member types, dived deep using the *average, min,* and *max ride length* in order to find other kind of possible trends.

### Data aggregation ###

  - Drilled the members type data by comparing counts between annual vs. casual members
  - Count number of each bikes type
  - Group by members and bikes type in order to find the total count
  - Count number of rides of weekday based on members type
  - Several other averages were calculated in order to find other kind of possible trends, like the average ride length by bike and member type and ride length for each member types based on week day


