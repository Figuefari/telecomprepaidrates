## Proyect description

We have the data to analyze two prepaid plans offered by the company. 
The objective will be to investigate the behavior of each tariff plan to determine which one generates higher revenue in order to adjust the advertising budget accordingly.

## Tasks

1. Open the data file and study the general information.
2. Prepare the data:
   - Convert to necessary types.
   - Find and eliminate data errors.
   For each user:
   - Find the number of calls made and minutes used per month.
   - Find the amount of SMS sent per month.
   - Find the volume of data per month.
   - Determine the monthly expenditure of each user.
3. Analyze the data to describe customer behavior and calculate statistical values.
4. Hypothesis testing to verify if the expenditure of users significantly differs according to the chosen plan; and hypothesis testing to determine if the average expenditure of New York - New Jersey users is different from users in other regions.
5. Overall conclusion of the data study.

## Description of the data
The company rounds seconds to minutes and megabytes to gigabytes. For calls, each individual call is rounded: even if the call lasted only one second, it will be counted as one minute. For web traffic, individual web sessions are not rounded. Instead, the total for the month is rounded up. If someone uses 1025 megabytes this month, they will be charged for 2 gigabytes.

The users table (data about users):
- user_id — unique identifier of the user
- first_name — user's first name
- last_name — user's last name
- age — user's age (in years)
- reg_date — subscription date (dd, mm, yy)
- churn_date — the date when the user stopped using the service (if the value is absent, the tariff was being used when these data were retrieved)
- city — user's city of residence
- plan — tariff name

The calls table (data about calls):
- id — unique identifier of the call
- call_date — call date
- duration — call duration (in minutes)
- user_id — user identifier making the call

The messages table (data about SMS):
- id — unique identifier of the SMS
- message_date — SMS date
- user_id — user identifier sending the SMS

The internet table (data about web sessions):
- id — unique identifier of the session
- mb_used — volume of data spent during the session (in megabytes)
- session_date — web session date
- user_id — user identifier

The plans table (data about tariffs):
- plan_name — tariff name
- usd_monthly_fee — monthly payment in US dollars
- minutes_included — included minutes per month
- messages_included — included SMS per month
- mb_per_month_included — included data per month (in megabytes)
- usd_per_minute — price per minute after exceeding package limits (for example, if the package includes 100 minutes, the operator will charge for minute 101)
- usd_per_message — price per SMS after exceeding package limits
- usd_per_gb — price per gigabyte of extra data after exceeding package limits (1 GB = 1024 megabytes)

## Table of contents

1. Initialization
   - Data Loading
   - Initial Data Exploration
     
2. Data Preprocessing
   - Missing Values
   - Duplicates
     
3. Data Enrichment

4. Data Analysis
   - Surf Plan Customers
   - Ultimate Plan Customers
     
5. Hypothesis Testing
   - First Hypothesis
   - Second Hypothesis
     
6. Conclusions

## Used libraries

- pandas 
- matplotlib
- scipy
- numpy
