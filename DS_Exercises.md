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
03.04.2026

#### Steps 8
Code: `list(users.columns)`.  
Columns attribute retrieves columns of the dataframe, used `list()` to convert it.

#### Steps 9
Code: `users.index`.  
Using index, returns how the data is indexed.

#### Steps 10
Code: `users.dtypes`.  
Attribute `dtypes` returns specific data type of each column.

#### Steps 11
Code: `users['occupation']`.  
Using brackets notation to print the occupation column.

### Steps 12-15 (Piotr)
3.04.2026

#### Step 12
Code: `users.occupation.drop_duplicates().count()`
Funtcion `drop_duplicates()` returns every unique occupation with an index where it apperars for the first time, while function `count()` counts that unique occupations and returns it as a number.

#### Step 13
Code: `users.occupation.value_counts().head(1)`
Fuction `value_counts` sorts dataset form the most frequent occupation to the rarest, with it's count, and function `head(1)` shows only the most frequent occupation.

#### Step 14
Code: `users.describe()`
Function `describe()` returns the count, mean, standard deviation which is the spread of the ages from the mean, 3 first quartiles which are the % of users below the given age, and also minimum and maximum value for integer columns.

#### Step 15
Code: `users.describe(include="all")`
Does the same thing as in last step but also for non integer columns, in  places where it can not count the functions it assigns NaN.
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
03.04.2026

#### Steps 7
Code: `discipline = euro12[['Team','Yellow Cards','Red Cards']]`.    
Passing a list of columns names inside the brackets and assigning it to a new dataframe.

#### Steps 8
Code: `discipline.sort_values(['Red Cards','Yellow Cards'])`.  
Passing a list to `sort_values()` sorts discipline by Red Cards primarily and uses Yellow Cards as the second key.

#### Steps 9
Code : `discipline.groupby('Team')['Yellow Cards'].mean()`.  
Groups the dataset by 'Team' and calculates the average number of 'Yellow Cards' for each team.

### Steps 10-12: (Piotr)
3.04.2026

#### Step 10
Code `euro12[euro12['Goals']>6]`
Only teams with more than 6 goals scored are shown.

#### Step 11
Code: `euro12[euro12.Team.str.startswith('G')]`
Function `str.startswith()` returns onlly teams that starts with give letter, in this example 'G'.

#### Step 12
Code: `euro12.iloc[:, 0:7]`
Using `iloc[]` to show only selected columns

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
03.04.2026  

Code: `drinks.groupby('continent')['wine_servings'].describe()`.  
Grouping by continent and using `describe()` to generate a full table of statistics.

#### Steps 6-7: (Kuba)
8:01 30.03.2026  

Code 6: `drinks.groupby("continent").mean(numeric_only=True)`.  
Code 7: `drinks.groupby("continent").median(numeric_only=True)`.  
Task completed with the usage of pandas "filename.groupby().median/mean()

#### Steps 8: (Piotr)
3.04.2026
Code: `drinks.groupby('continent').spirit_servings.agg(['mean', 'min', 'max'])`
Using `group.by` to group dataset by continents, then `agg()` to apply those 3 fuctions at once
