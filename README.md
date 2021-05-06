# ANALYZE SUPERMARKET DATA ACROSS THE COUNTRY - COMPANY XYZ
The project is used to analyzed XYZ Supermarket data. XYZ has branches in 3 states in Nigeria: Lagos, Abuja and Port Harcourt. The project is aimed at helping the company understand sales trends and determine its growth.

## Overview of the Project

### Step 1: Loading the dataset.
The datasets from the three branches is first combined together using the glob library.
The combined data is saved in my directory as Combined Data.csv and it is loaded to pandas using the pd.read_csv() method. It is then saved as "data" in pandas

### Step 2: Data Exploration
Several libraries are imported to help with data exploration and they are: pandas, numpy, matplotlib, seaborn and warnings. 
1.	The head() function is used to read the first few rows of the dataset
2.	The number of rows and columns are checked using the shape attribute
3.	Also, the names of the columns in the datasets are checked using the columns method
4.	The general statistical summary is checked using the describe function
5.	A more detailed summary is accessed using the info function
6.	The data is checked for the presence of missing values using the isnull() function and is found to be free of missing values.

### Step 3: Dealing with Date and Time Features
The dataset has 2 columns, Date and Time which had the Object data type. The data type has to be changed using the  pandas .to_datetime() feature to enable them become datetime data types. This  is done using pd.to_datetime().
Similarly, new columns are created from date and time. These columns are day, month and year, containing the day month and year found in the data column. Also, a new column, hour is created from the time column and named hour.
The unique method is used to find the number of unique hours in the Hour column.

### Step 4: Unique Values in Columns
Categorical Columns (Columns that have the Object data type) are gotten and their unique values are also derived using the unique(), nunique() and value_counts() functions. 

### Step 5: Group by Aggregations
The Group By function is also explored and they following were obtained:
•	The City Column was grouped and aggregated by Mean and Sum
•	The City with the highest total gross income, highest unit price and highest quantity were obtained.

### Step 6: Data Visualization
Seaborn Visualization Library is used to graphically explore the dataset. The Branch, City and Payment Columns are explored using Seaborn’s countplot to determine the most frequent.  The Product Line is also explored to determine the Highest and Lowest Sold product line.
Similarly, a countplot of the product line grouped by the Payment method using Hue is visualized, as well as the Payment method grouped by the Branch. Other columns were also visualized using Bar plot, Catplot, Bar Chart and Seaborn’s distplot to check the distribution of the Unit Price column.

## Future Work
Predictive Analysis could be included.

## Stand out Session
Additional plots were included such as the Bar Chart for Quanity Column, the dist plot for the Unit price column, the identify if the column is normally distributed (This would be more useful in prediction), Also, the figsize attribute was included to make the chart more visible.
