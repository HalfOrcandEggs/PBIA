Working with DAX
================

Exercise 2: Budget vs Actuals
-----------------------------

#### Scenario

##### Budget: Different Granularity

>   For this example, instead of the budget data, we have Sales Quotas which are
>   under a different granularity. The concept and principles remain the same.
>   we have a table with a different granularity which we want to connect to
>   this model. The Sales Quota has the quota of sales for each employee in each
>   quarter. The granularity of this table is per employee and per quarter,
>   while the granularity of the sales table is per employee, per day, and per
>   combination of SalesTerritory and Product also.

>   If you get the FactSalesQuota from the AdventureWorksDW, you will notice
>   that there is a Date column, and the DateKey, which I have removed in my
>   example below, because they will be confusing for you to understand the
>   table is showing quarterly data (we will calculate the date key later on in
>   this lab exercise.

>   Here is how the data in the Sales Quota table looks like: (FactSalesQuota in
>   the AdventureWorksDW)

>   The main tasks for this exercise are as follows:

-   Get Data.

-   Add a new column for the datekey

-   Compare Quotas to Actual Sales.

>   Estimated Time to complete: 15 min

##### Challenges of Two Different Granularities

If you want to build the star schema for Sales Quota and Sales (similar to
Actual vs Budget), then the challenge would be;

-   How to connect The Sales Quote to the date table?

-   If I create a Quarter dimension, then how to connect Quarter dimension to
    the date dimension? does this create a snowflake scenario?

I’m going to explain an easy method to solve it and then it will be a proper
star schema again.

#### Task 1: Get Data

1.  Start the Power BI Desktop and create a new blank query

2.  Open the advanced editor and re0place the query with the following

#### Task 2: Add a new column<br>

1.  Manually code a SQL Server connection

#### Task 3: Connect SalesQuota to the Date Table

Although the sales quota information is quarterly based, you can still connect
it to the date table. This would avoid creating an extra dimension for the
quarter and snowflake between quarter dimension and the date dimension. The only
thing to consider is that you have to consider a specific date in each quarter
as your default value. For example, we can consider the first day of each
quarter as our date value.

To achieve, this purpose, we need to create a column in the SalesQuota table
with has the DateKey in it (the DateKey used in my sample is in this format
YYYYMMDD), so It can be something like 20190101, 20190401, and etc). This is
what we are going to build in this part:

1.  The specific date of each quarter will be the 1st of the 1st month in that
    quarter

2.  Use a text field to create the date key YYYYMMDD.

Go hard

Slice dice and so the fancies.

End of Exercise
