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
        1. Question 1 | What the best month for sales ?
        2. Question 2 | What city had the highest number of values ?
        3. Question 3 | What time should we display advertisements to maximize the likelihood of customer's buying product
        4. Question 4 | What products are most often sold together ?
        5. Question 5 | What product sold the most ? why do you think it sold the most ?
        
## Analytical Approach 
1. Question 1 | What the best month for sales ?
    - we use groupby() method to split data into groups based on 'Month' column that has been added using sum() method
    - we use bar plot to visualize the results
    - number of Months act as X - axis, meanwhile amount of sales act as Y - axis
    - target the highest value from bar plot then give the different color to it
    - interpret the results
2. Question 2 | What city had the highest number of values ?
    - we use groupy() method to split data into groups based on 'City' column that has been added using sum() method
    - we use for loop to iterating over a list sequence from df_sales.groupby('City') as 'cities' variable
    - we use bar plot to visualize the results
    - name of city act as X - axis, meanwhile amount of sales act as Y - axis
    - target the highest value from bar plot then give the different color to it
    - interpret the results
3. Question 3 | What time should we display advertisements to maximize the likelihood of customer's buying product
    - we use groupby() method to split data into groups based on 'Hour' column that has been calculated using count() method
    - we use for loop to iterating over a list sequence from df_sales.groupby('Hour') as 'hours' variable
    - we use line plot to visualize the results
    - Hour act as X - axis, meanwhile number of orders act as Y - axis
    - peak in X - axis of line graphs can be interpreted as results (see red X plot)
    - interpret the results
4. Question 4 | What products are most often sold together ?
    - we use duplicated ()(keep=False) method from Order ID columns. It marks all duplicates as true and allows us to see all duplicate rows
    - We create 'Grouped' column from df_sales.groupby('Order Id')['Product'].transform(lambda x: ','.join())
    - we use drop_duplicates() method from df_sales[['Order ID', 'Grouped']]
    - we determine how many products to display using for loop in df_sales['Grouped'] then update data using update() method from Counter and Combinations class
5. Question 5 | what product sold the most ? why do you think it sold the most ?
    - we use groupby() method to split data into groups based on 'Product' column as 'product_group'
    - we use sum() method to add values from list 'Quantity Ordered' in 'product_group' as 'quantity_ordered' variable
    - we use for loop to iterating over a list sequence 'Product' from product_group as 'products' variable
    - we use bar plot to visualize the results
    - name of Product act as X - axis, meanwhile amount of Quantity Ordered act as Y - axis
    - target the highest value from bar plot then give the different color to it
    - interpret the results
    - correlation with deeper analysis using 'Price Each' column as line graphs from df_sales.groupby('Product').mean()['Price Each'] as Y2 - axis
    
## Results
1. The best selling month occurs in the 12th month (December) : 4613443.34
2. The best selling city occurs in San Fransisco (CA) : 10304443952
3. 13 and 20 pm are the right time to display advertisements
4. Iphone and lightning charging cable are products that most often sold together
5. AAA Batteries (4 - Pack) is best selling product, it because cheap and mostly needed
