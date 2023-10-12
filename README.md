# Awishcar Assignment

## Problem Statements

1. A has data which has been changed into date, figure out what should be the format of the data through adjacent cells		
2. Column B, C, D and E represent the address and should be in proper format( 1st letter of the word should be CAPITAL)		
3. Column F- there are iregular space in the between the  names		
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

### We are using Python (Jupyter Notebook) with Pandas, Numpy and ReGex for EDA and Data Cleaning.  

### IMP NOTE: Wherever we saw -1 in the cleaned CSV file, it represents a Missing Value.

### 1. Read The Google Sheet
1. Read the Google Sheet as a CSV file using Pandas from its sharing link.
2. Load it as a Pandas Dataframe.
3. If required, save the CSV file to the Local Computer.
4. Use the info() function to check the number of rows, number of columns, column names, number of null values and data types of all the columns.
5. isnull().sum() function will give us the sum of all Null or NAN or Missing values column-wise.
 
### Parcel ID

**The data in Parcel ID is changed to Date**

**We assume that the parcel ID is a continuous alphanumeric number.**

1. Write a function to convert the month name into the month number.
2. By assuming parcel ID as a continuous alphanumeric number remove the hyphen and get a continuous alphanumeric number as Parcel Number.









