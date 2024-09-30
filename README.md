# Movie Data Analysis using Pivot Tables

Data Formatting is an integral part of any analysis before the analysis is done on the dataset. In this document, I have mentioned my approach to data analysis with the help of spreadsheets. Broadly we can classify my approach into two steps as shown below:

## Step 1: Data Formatting
* [Checking the data for inconsistencies](#Checking-the-data-for-inconsistencies)
* [Converting the formats](#Converting-the-formats)
* [Splitting or Combining different columns](#Splitting-or-Combining-different-columns)
* [Converting numbers into Percentage](#Converting-numbers-into-Percentage)

## Step 2: Analysis using Pivot Tables
* [Asking the right questions](#Asking-the-right-questions)
* [Data Visualization](#Data-Visualization)

## Data Formatting

### Checking the data for inconsistencies 

As we can see the table consists of values which represent currency in column M and column N as we cannot see the units. To make the data more accurate we can add the currency symbol to our column using the tools provided by Google spreadsheets. This makes our task easier and eliminates the need to format the data manually.

![image](https://github.com/user-attachments/assets/45187b91-9ebe-4095-93bf-6815bd1430ad)

![image](https://github.com/user-attachments/assets/52631ce8-bea8-461c-bb7c-d0252f64d5a5)

### Converting the formats

As we know dates are often a critical part of data analysis and entering dates correctly is essential to ensure accurate results. However, formatting dates such that it is easy to understand is equally important to ensure the correct interpretation of those results. To do that let's use the ```TEXT()``` to convert the dates into a more easy-to-read format.

![image](https://github.com/user-attachments/assets/96bbfb1f-3996-434d-86c5-718320b589f4)

![image](https://github.com/user-attachments/assets/e344da4c-88e8-43d2-9fca-9f4bc77bb910)

### Splitting or Combining different columns

In our movie dataset, we have a sheet named "Directors" where we have their first and last names listed together. To split the names into two different columns we can use the tool provided by Google spreadsheet and work towards our analysis.

![image](https://github.com/user-attachments/assets/6877b949-eb04-489d-9641-a5ad441a4756)

![image](https://github.com/user-attachments/assets/4e2507d8-9921-491d-a17f-d437dc978a0b)

![image](https://github.com/user-attachments/assets/0cefb565-acab-40ec-b147-854995877440)

The use of a separator is essential in such kind of data formatting. As we can see this has resulted in the names being divided into three columns which are now easier to understand.

In scenarios where we need to merge the columns, we can use the ```Concatenate()``` function that makes our task very efficient.

![image](https://github.com/user-attachments/assets/b9f2d955-5382-4140-b1bd-c4398537f3ab)

![image](https://github.com/user-attachments/assets/2619b846-b2b8-4080-ae15-aef5fe336af7)

### Converting numbers into Percentage

The percentage is used to evaluate extensive data and hence presents an accurate value. It is important for data management and analysis as it helps calculate profit and loss. To convert numbers into percentages in Google spreadsheets we can use ```To_Percent()`` as shown below:

![image](https://github.com/user-attachments/assets/99aa61b7-4595-4e2d-b2bb-c3ea48f9fa53)

![image](https://github.com/user-attachments/assets/4b56de92-fdf3-4c00-894d-569d474eac64)

## Analysis using Pivot Tables

### Asking the right questions

**I. What was the total revenue generated each year?**
   
Instead of creating a formula to calculate the revenue per year, we can use a pivot table. It helps keep our calculations in one place and the rest of the data separate. First, we will select the release date column in the pivot table editor to do our analysis. The data in each cell is each day a movie was released. We can group these dates into individual years for more accuracy in our analysis.

![image](https://github.com/user-attachments/assets/2ab89821-44f4-40ea-92a2-8d486491b3f1)

![image](https://github.com/user-attachments/assets/fec8cf3b-e1f9-414d-890e-0600e3f9259f)

The rows represent each year the movie was released and we can add values to each of these rows.

![image](https://github.com/user-attachments/assets/8a2d1987-8a01-47f8-8ca9-7038b4b62776)

[! These calculations are automatic because the pivot table is already set to summarize the data using the sum function. Exploring other functions such as the MIN function to see the minimum revenue each year and ```COUNT``` for the number of movies generated the revenue each year ]

**Conclusion:** As we can see the year 2014 had the highest revenue while 2016 had the lowest. 

**II. What will be the conclusion if we use the Average function instead of the Sum?**

![image](https://github.com/user-attachments/assets/51897b07-cb3a-406e-a747-3b0c6992e6e9)

**Conclusion:** The average function shows the year 2015 had the lowest revenue generated. 

**III. Why did this number differ so much? Which function can let us find out the reason for this outlier?**

![image](https://github.com/user-attachments/assets/804c393c-7c24-40cf-a428-ee7cd7181beb)

The above table shows that in the year 2015, the highest number of movies were released but  the same year seems to have the second lowest total revenue generated. This concludes the movies in 2015 didn't earn that much on the releases as compared to other year movies.

Furthermore, we can use the FILTER tool to find out what number of movies contributed to a revenue below 10M in a particular year. Let's start this by 
copy-pasting the table and rename the columns.

![image](https://github.com/user-attachments/assets/cd263f59-5070-4591-b16a-60ab6dc79f50)

![image](https://github.com/user-attachments/assets/49d8f1ca-9e35-4373-a10e-2bc55f56a9d1)

![image](https://github.com/user-attachments/assets/b3a0bde2-94d6-44b5-b360-607a7f645f2c)

Now we know that 20 movies in 2015 made less than $10M. To verify our average column let's create a calculated field.

![image](https://github.com/user-attachments/assets/70daaddc-a357-42a7-8472-ea871f98c407)

By doing this we get to know the calculations are accurate and the values in this new table will come below $10M. We can go ahead to see the contribution of movies in terms of percentages too.

![image](https://github.com/user-attachments/assets/5bf26038-f1c6-4414-9325-0101a13eadad)

**Conclusion:** The calculation shows that 16.3% of the movies in 2015 generated less than $10M which pretty much sums up the reason why we have the overall sum of revenue generated for 2015 low.

**IV. On average, how much money do movies make in each genre?**

**Result:**
![image](https://github.com/user-attachments/assets/1d94c6ce-5571-4cfd-8c0f-7599ea765a81)

**V. On average, how much money is spent on a movie broken by genre?**

**Result:**
![image](https://github.com/user-attachments/assets/27c31ce6-bdcf-4c16-b0bf-e38fec69e61a)

**VI. On average, which genre has the most profitable movies?**

**Result:**
![image](https://github.com/user-attachments/assets/e2a47dc2-20c4-4c49-a3cb-ea48ba10f598)

![image](https://github.com/user-attachments/assets/15efb314-4db0-47de-a60d-048634374470)

![image](https://github.com/user-attachments/assets/79a01c5f-8622-41d1-95b4-eb3fec7b10a5)

### Data Visualization 

After following the data formatting and other analytical steps above, we can represent the whole dataset as shown below. The graph represents a snapshot of the entire dataset and allows us to infer information about various genres and their respective box office revenue. 

![image](https://github.com/user-attachments/assets/7539b86e-e898-4046-9725-e25d71accb2c)
