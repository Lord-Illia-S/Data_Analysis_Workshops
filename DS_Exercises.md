## Exercise 1: Getting and Knowing your Data

### Step 1-3:
Data Import and loaded dataset

### Steps 4-7: (Illia)
01.04.2026

#### Steps 4
Code: `users.head(25)`.  
Function `head()` return top rows from the table.

#### Steps 5
Code: `users.tail(25)`.  
Function `tail()` return last rows from the table.

#### Steps 6
Code: `len(users)`.  
Function `len()` return the length of the object. In this case, it returns the number of observations.

#### Steps 7
Code: `len(users.columns)`.  
In this case, function `len()` return the number of columns.

### Steps 8-11 (Mateusz)

### Steps 12-15 (Piotr)

### Steps 16-18 (Kuba)


30.03.2026 - 7:51

#### Ex 16 & 17
Code 16: `users.agg({'occupation': 'sum'})`.  
Code 17: `users.agg({'age': 'mean'})`.  
Completed using pandas agg


#### Ex 18
Code: `users['age'].value_counts().sort_values().head(5)`.  
Used `head(5)` becasue only these values appear Once, the rest twice


## Exercise 2: Filtering and Sorting Data

### Step 1-3:
Data Import and loaded dataset

### Steps 4-6: (Illia)
01.04.2026

#### Steps 4
Code: `euro12.Goals`.  
Just selecting the `Goals` column.

#### Steps 5
Code: `len(euro12.Team)`.  
`len()` return the number of teams.

#### Steps 6
Code: `len(euro12.columns)`.  
Function `len()` return the number of columns (similarly to step 7 in Ex 1).

### Steps 7-9: (Mateusz)

### Steps 10-12: (Piotr)

### Steps 13-14: (Kuba)
30.03.2026 - 7:58

#### Step13
Code: `euro12.iloc[:, :-3]`.  
`-3` so the last 3 columns are removed

#### Step 14
Code: `euro12.iloc[[3, 7, 12], 4]`.  
Also completed with 'filename.iloc'


## Exercise 3: GroupBy

#### Step 1-3:
Data Import and loaded dataset

#### Steps 4 (Illia)
01.04.2026

Code: `drinks.sort_values(by='beer_servings').tail(1)`.  
At first, we sort the values in beer_servings column, after that get the last number.

#### Steps 5: (Mateusz)

#### Steps 6-7: (Kuba)
8:01 30.03.2026  

Code 6: `drinks.groupby("continent").mean(numeric_only=True)`.  
Code 7: `drinks.groupby("continent").median(numeric_only=True)`.  
Task completed with the usage of pandas "filename.groupby().median/mean()

#### Steps 8: (Piotr)
