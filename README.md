# Awishcar Assignment

## Problem Statements

1. A has data which has been changed into date, figure out what should be the format of the data through adjacent cells		
2. Column B, C, D and E represent the address and should be in proper format( 1st letter of the word should be CAPITAL)		
3. Column F- there are irregular spaces in between the names		
4. Column H&I should be stored as id , hence create the id of your own		
5. Column J needs to be split into first name and last name		
		
#### Following are the target columns	
Please map these fields to the column in Sheet 1
1. Permit 	
2. Parcel number		
3. Location		
4. Bussiness Name		
5. B Type Id		
6. B Use id		
7. Applicant First Name		
8. Applicant Last Name		
		
Figure if any pattern exists between Column G and remaining columns		
		
The cells which are missing data need to be notified to the customer, figure out a way to give insight to the about missing data.

## Exploratory Data Analysis (EDA) and Data Cleaning

We are using **Python (Jupyter Notebook)** with **Pandas, Numpy** and **ReGex** for **EDA** and **Data Cleaning.**  

**IMP NOTE**: **Wherever** we saw **-1** in the **cleaned CSV file**, it represents **a Missing Value.**

### 1. Read The Google Sheet
1. Read the Google Sheet as a CSV file using Pandas from its sharing link.
2. Load it as a Pandas Dataframe and view a few rows.
3. If required, save the CSV file to the Local Computer.
4. Use the info() function to check the number of rows, number of columns, column names, number of null values and data types of all the columns.
5. The isnull().sum() function will give us the sum of all Null or NAN or Missing values column-wise.
 
### 2. Parcel ID

**The data in Parcel ID is changed to Date**

**We assume that the parcel ID is a continuous alphanumeric number.**

1. Write a function to convert the month name into the month number.
2. By assuming parcel ID as a continuous alphanumeric number remove the hyphen and get a continuous alphanumeric number as a Parcel Number.

### 3. Location

The Location column has to be created using 4 columns Street1, Street2, City and St.

1. Replace NAN values with a blank in all 4 columns.
2. Use title() function to make 1st letter of the word as CAPITAL.
3. Join all 4 columns and name the new column as Location.
4. Among Street1, City and St, if any one of them is missing then replace the Location with -1.
5. Delete all 4 columns as we no longer need them.

### 4. Contractor_Name

1. Use ReGex to remove irregular spaces between the names.
2. Replace missing values with -1.

### 5. Type and SubType

1. Create a Type ID column for Type using the Pandas factorize() function.
2. Create a SubType ID column for SubType using the Pandas factorize() function.
3. If NAN is present in Type or SubType then it will be represented as -1 in Type ID or SubType ID.
4. Check for unique IDs in Type and SubType.

### 6. Primary_Contact

1. Replace NAN in Primary_Contact with -1.
2. Write a function to get the First Name from Primary_Contact and make it a new column.
3. Write a function to get the Last Name from Primary_Contact and make it a new column.
4. Delete Primary_Contact as we no longer need it.

### 7. PermitNum

1. Replace missing values with -1.

### 8. Renaming the columns and Download the Cleaned CSV file

1. Rename PermitNum as Permit
2. Rename Parcel_ID as Parcel Number
3. Rename Contractor_Name as Bussiness Name
4. Rename Type_ID as B Type ID
5. Rename SubType_ID as B Use ID
6. Rename First_Name as Applicant First Name
7. Rename Last_Name as Applicant Last Name
8. Download the Cleaned CSV file to local computer.

## To Run the Awishcar.ipynb file on Google Colab
1. Download the file Awishcar.ipynb from above.
2. Open https://colab.research.google.com 
3. Sign in into Google account.
4. Upload the file Awishcar.ipynb.
5. Run the programe block by block to see the output.

## Changes in new Updated file
1. In Parcel Id the long for loop is replaced with a shorter nested for loop.
2. In Location, earlier we were replacing it with -1 only when the full location was empty.
3. Now among Street1, City and St, if any one of them is missing then replace the Location with -1.
4. In Last Name, in some cases 'Jr' appeared as it was their last name. It is also taken care of in the new code.

## Visual/Graphical Representation of Missing Data

There are 3 best methods to plot Missing Data.

### 1. Bar Chart 
This bar chart gives you an idea of how many missing values are there in each column.

![bar](Bar.png)

### 2. Matrix
Using this matrix we can very quickly find the pattern of missingness in the dataset.

![m](Matrix.png)

### 3. Heatmap
The heatmap shows the correlation of missingness between every 2 columns.

![h](Heatmap.png)

### Now let us jump into Jupyter Notebook
