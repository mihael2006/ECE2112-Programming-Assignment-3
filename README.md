# ECE2112-Programming-Assignment-3
**Introduction to Python Programming**

Name: Padilla, Erich S. 

Section: 2ECE-C

Date Submitted: September 16, 2025

# Description
In this programming assignment, we apply what we learned in Pandas to explore the cars.csv dataset. The dataset contains various car models along with details such as fuel efficiency, engine size, horsepower, weight, and transmission type.

# Problem 1
The first thing to do is we'll let the program read or load the ```cars.csv``` file, which contains data that we're going to do some demonstration. This can be done using this ```pd.read_csv()``` syntax, as long as it is in the same directory.
```python
cars = pd.read_csv('cars.csv')
cars
```
Now, to display the first five rows or even the last five rows of the data set, we can use ```cars.head()``` for the first five rows, and ```cars.tail()``` for the last five rows. This can be changed however you like, for example, you wanted to display the first 10 or last 10 rows, all you need to do is input the 10 inside the parenthesis.
```python
cars.head(10)
cars.tail(10)
```
