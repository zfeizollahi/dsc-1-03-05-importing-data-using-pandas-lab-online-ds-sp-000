
# Importing Data Using Pandas - Lab

## Introduction

In this lab, you'll get some practice with loading files with summary or metadata, and if you find that easy, the optional "level up" content covers loading data from a currupted csv file!

## Objectives
You will be able to:
* Import data from csv files and Excel files
* Understand and explain key arguments for imports
* Save information to csv and Excel files
* Access data within a Pandas DataFrame (print() and .head())

#  Loading Files with Summary or Meta Data

Load either of the files Zipcode_Demos.csv or Zipcode_Demos.xlsx. What's going on with this dataset? Clean it up into a useable format and describe the nuances of how the data is currently formatted.

All data files are stored in a folder titled 'Data'.


```python
#Your code here
import pandas as pd
demos = pd.read_excel('/Users/zhaleh/flatiron/section01/dsc-1-03-05-importing-data-using-pandas-lab-online-ds-sp-000/Data/Zipcode_Demos.xlsx', skiprows=48)
zipcode_df = pd.DataFrame(demos)
zipcode_df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>JURISDICTION NAME</th>
      <th>COUNT PARTICIPANTS</th>
      <th>COUNT FEMALE</th>
      <th>PERCENT FEMALE</th>
      <th>COUNT MALE</th>
      <th>PERCENT MALE</th>
      <th>COUNT GENDER UNKNOWN</th>
      <th>PERCENT GENDER UNKNOWN</th>
      <th>COUNT GENDER TOTAL</th>
      <th>PERCENT GENDER TOTAL</th>
      <th>...</th>
      <th>COUNT CITIZEN STATUS TOTAL</th>
      <th>PERCENT CITIZEN STATUS TOTAL</th>
      <th>COUNT RECEIVES PUBLIC ASSISTANCE</th>
      <th>PERCENT RECEIVES PUBLIC ASSISTANCE</th>
      <th>COUNT NRECEIVES PUBLIC ASSISTANCE</th>
      <th>PERCENT NRECEIVES PUBLIC ASSISTANCE</th>
      <th>COUNT PUBLIC ASSISTANCE UNKNOWN</th>
      <th>PERCENT PUBLIC ASSISTANCE UNKNOWN</th>
      <th>COUNT PUBLIC ASSISTANCE TOTAL</th>
      <th>PERCENT PUBLIC ASSISTANCE TOTAL</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>10001</td>
      <td>44</td>
      <td>22</td>
      <td>0.50</td>
      <td>22</td>
      <td>0.50</td>
      <td>0</td>
      <td>0</td>
      <td>44</td>
      <td>100</td>
      <td>...</td>
      <td>44</td>
      <td>100</td>
      <td>20</td>
      <td>0.45</td>
      <td>24</td>
      <td>0.55</td>
      <td>0</td>
      <td>0</td>
      <td>44</td>
      <td>100</td>
    </tr>
    <tr>
      <th>1</th>
      <td>10002</td>
      <td>35</td>
      <td>19</td>
      <td>0.54</td>
      <td>16</td>
      <td>0.46</td>
      <td>0</td>
      <td>0</td>
      <td>35</td>
      <td>100</td>
      <td>...</td>
      <td>35</td>
      <td>100</td>
      <td>2</td>
      <td>0.06</td>
      <td>33</td>
      <td>0.94</td>
      <td>0</td>
      <td>0</td>
      <td>35</td>
      <td>100</td>
    </tr>
    <tr>
      <th>2</th>
      <td>10003</td>
      <td>1</td>
      <td>1</td>
      <td>1.00</td>
      <td>0</td>
      <td>0.00</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>100</td>
      <td>...</td>
      <td>1</td>
      <td>100</td>
      <td>0</td>
      <td>0.00</td>
      <td>1</td>
      <td>1.00</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>100</td>
    </tr>
    <tr>
      <th>3</th>
      <td>10004</td>
      <td>0</td>
      <td>0</td>
      <td>0.00</td>
      <td>0</td>
      <td>0.00</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>...</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0.00</td>
      <td>0</td>
      <td>0.00</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>10005</td>
      <td>2</td>
      <td>2</td>
      <td>1.00</td>
      <td>0</td>
      <td>0.00</td>
      <td>0</td>
      <td>0</td>
      <td>2</td>
      <td>100</td>
      <td>...</td>
      <td>2</td>
      <td>100</td>
      <td>0</td>
      <td>0.00</td>
      <td>2</td>
      <td>1.00</td>
      <td>0</td>
      <td>0</td>
      <td>2</td>
      <td>100</td>
    </tr>
    <tr>
      <th>5</th>
      <td>10006</td>
      <td>6</td>
      <td>2</td>
      <td>0.33</td>
      <td>4</td>
      <td>0.67</td>
      <td>0</td>
      <td>0</td>
      <td>6</td>
      <td>100</td>
      <td>...</td>
      <td>6</td>
      <td>100</td>
      <td>0</td>
      <td>0.00</td>
      <td>6</td>
      <td>1.00</td>
      <td>0</td>
      <td>0</td>
      <td>6</td>
      <td>100</td>
    </tr>
    <tr>
      <th>6</th>
      <td>10007</td>
      <td>1</td>
      <td>0</td>
      <td>0.00</td>
      <td>1</td>
      <td>1.00</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>100</td>
      <td>...</td>
      <td>1</td>
      <td>100</td>
      <td>1</td>
      <td>1.00</td>
      <td>0</td>
      <td>0.00</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>100</td>
    </tr>
    <tr>
      <th>7</th>
      <td>10009</td>
      <td>2</td>
      <td>0</td>
      <td>0.00</td>
      <td>2</td>
      <td>1.00</td>
      <td>0</td>
      <td>0</td>
      <td>2</td>
      <td>100</td>
      <td>...</td>
      <td>2</td>
      <td>100</td>
      <td>0</td>
      <td>0.00</td>
      <td>2</td>
      <td>1.00</td>
      <td>0</td>
      <td>0</td>
      <td>2</td>
      <td>100</td>
    </tr>
    <tr>
      <th>8</th>
      <td>10010</td>
      <td>0</td>
      <td>0</td>
      <td>0.00</td>
      <td>0</td>
      <td>0.00</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>...</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0.00</td>
      <td>0</td>
      <td>0.00</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>9</th>
      <td>10011</td>
      <td>3</td>
      <td>2</td>
      <td>0.67</td>
      <td>1</td>
      <td>0.33</td>
      <td>0</td>
      <td>0</td>
      <td>3</td>
      <td>100</td>
      <td>...</td>
      <td>3</td>
      <td>100</td>
      <td>0</td>
      <td>0.00</td>
      <td>3</td>
      <td>1.00</td>
      <td>0</td>
      <td>0</td>
      <td>3</td>
      <td>100</td>
    </tr>
  </tbody>
</table>
<p>10 rows × 46 columns</p>
</div>



The data doesn't start until line 48, the first 47 rows are summary statistics in row format (each stat is on a new row) rather than on a single row lining up with the data points.

## Level Up (Optional)

### Loading Corrupt CSV files

Occassionally, you encountered some really ill formatted data. One example of this can be data that has strings containing commas in a csv file. Under the standard protocol, when this occurs, one is suppossed to use quotes to differentiate between the commas denoting fields and commas within those fields themselves. For example, we could have a table like this:  

ReviewerID,Rating,N_reviews,Review,VenueID
123456,4,137,This restuarant was pretty good, we had a great time.,98765

Which should be saved like this if it were a csv (to avoid confusion with the commas in the Review text):
"ReviewerID","Rating","N_reviews","Review","VenueID"
"123456","4","137","This restuarant was pretty good, we had a great time.","98765"

Attempt to import the corrupt file, or at least a small preview of it. It is appropriately titled Yelp_Reviews_corrupt.csv. Investigate some of the intricacies of skipping rows to then pass over this error and comment on what you think is going on.


```python
#Hint: here's a useful programming pattern to use.
try:
    #do something
except Exception as e:
    #handle your exception e
```


```python
#Your code here
```
