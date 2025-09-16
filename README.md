# ECE2112-Programming-Assignment-3
**Introduction to Python Programming**

Name: Padilla, Erich S. 

Section: 2ECE-C

Date Submitted: September 16, 2025

# Description
In this programming assignment, we apply what we learned in Pandas to explore the cars.csv dataset. The dataset contains various car models and details such as fuel efficiency, engine size, horsepower, weight, and transmission type.

# Problem 1
The first thing to do is let the program read or load the ```cars.csv``` file, which contains data that we will use for some demonstration. This can be done using this ```pd.read_csv()``` syntax, as long as it is in the same directory.
```python
cars = pd.read_csv('cars.csv')
cars
```
Now, to display the first five rows or even the last five rows of the data set, we can use ```cars.head()``` for the first five rows, and ```cars.tail()``` for the last five rows. This can be changed, however you like. For example, if you want to display the first 10 or last 10 rows, all you need to do is input the 10 inside the parentheses.
```python
cars.head(10)
cars.tail(10)
```
# Problem 2
Using the same dataset, we'll load it again in the program before we do subsetting, slicing, and indexing operations. Since the problem requires getting the odd-numbered columns for the first five rows, we can use ```df.iloc[row_start:row_end, col_start:col_end:step]``` to selects rows from the first row up to (but not including) last row, and first column to the last row (or the end if omitted), moving in steps of step.
```python
cars.iloc[1:6, 1::2]
```
Next, the code we can use is below to display the row containing the ‘Model’ of ‘Mazda RX4’.
```python
cars[cars['Model']=='Mazda RX4']
```
This basically says that from the dataframe cars, filter rows where the Model column equals "Mazda RX4", and return only those rows. On the other hand, in finding how many cylinders (‘cyl’) does the car model ‘Camaro Z28’ have, the code below is a way to get it, which says that from the dataframe cars, find the row(s) where the Model column equals "Camaro Z28", and from those rows, return only the Model and cyl columns. So instead of the whole row, you get a smaller table with the car’s name and cylinder count.
```python
cars.loc[cars['Model'] == "Camaro Z28", ['Model', 'cyl']]
```
Finally, to Determine how many cylinders (‘cyl’) and what gear type (‘gear’) do the car models ‘Mazda RX4 Wag’, ‘Ford Pantera L’ and ‘Honda Civic’ have, we can make it first as a list before we keep only the rows where the Model is in the models list, and then show only the Model, cyl, and gear columns.
```python
models = ['Mazda RX4 Wag', 'Ford Pantera L', 'Honda Civic']
cars.loc[cars['Model'].isin(models),['Model', 'cyl', 'gear']]
```

# Version History
* v.01








