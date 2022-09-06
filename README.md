# Sales Data Analysis - Electronic Store (study case)

### Data Analyst Projects #1

##### Author : Achmad Adyatma Ardi
##### Email : achmad541997@gmail.com
##### IG : [@adyatmaardi](https://www.instagram.com/adyatmaardi/?hl=id)

## Prerequisites
1. Install Jupyter Notebook
2. Install necessary Python-module

  - [OS](https://pypi.org/project/os-sys/) (built - in) module - it provides for creating and removing a directory (folder), fetching its contents, changing and identifying the currect directory, etc.

           pip install os-sys


   - [pandas](https://pypi.org/project/pandas/) module - it makes you to use high-performance data structures and data analysis tools.
   
           pip install pandas
   
   
   - [datetime](https://pypi.org/project/DateTime/) module - it supplies classes for manipulating dates and times. 

           pip install DateTime

   - [matplotlib](https://matplotlib.org/stable/users/installing/index.html) module - It used to create 2D graphs and plots by using python scrips. It makes things easy for plotting by providing feature to control line styles, font properties, formatting axes etc.

           python -m pip install -U matplotlib

   - [seaborn](https://numpy.org/install/) module - It used for making statistical graphics in python. It builds on top of matplotlib and integrates closely with pandas data structures. Seaborn helps you explore and understand your data

           pip install seaborn
           
   - From itertools import [combinations](https://pypi.org/project/warn/) (built - in) module - It is a collection of the element where the order doesn't matter. Python itertools module provide the combination() method to calculate the combination of given data.

           pip install combination-py
   
   - From collections import [Counter](https://pypi.org/project/warn/) (built - in) module - It is a subclass of dict that's specially designed for counting hashable objects in Python. It's a dictionary that stores objects as keys and counts as values. To count with Counter, you typically provide a sequence or iterable of hashable objects as an argument to the class's constructor

           pip install Counter
   
   - [warnings](https://pypi.org/project/warn/) (built - in) module - It used to control how the warnings should be treated.

           pip install warn


## Objectives
1. To do analysis for sales purposes
2. Step
    - Task #1 | Merge 12 months of sales data into one csv file
    - Task #2 | Clean up data
        1. Remove of NaN (Not a Number) values
        2. Dealing with datetime column 'Order Date'
        3. Convert original dataset columns to the correct type
        4. Augmenting data with additional needed columns
            - Month column - int64
            - Sales column - float64
            - City column - 'string'
            - Hour column - int64
            - Minute column - int64
            - Count column - int64
    - Task #3 | Analysis - Answer 5 important questions
        1. What the best month for sales ?
        2. What city had the highest number of values ?
        3. What time should we display advertisements to maximize the likelihood of customer's buying product
        4. What products are most often sold together ?
        5. What product sold the most ? why do you think it sold the most ?
        
## Analytical Approach
- Question #1 What the best month for sales ?
- Question #2 What city had the highest number of values ?
- Question #3 What time should we display advertisements to maximize the likelihood of customer's buying product
- Question #4 What products are most often sold together ?
- Question #5 What product sold the most ? why do you think it sold the most ?

