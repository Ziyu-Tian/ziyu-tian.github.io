# Python Data Analysis 
## I: Import the relevant Python Libraries 
```python 
# Import 'display' in 'Ipython.display'
from IPython.display import display
import os 
from pathlib import Path # OS and Pathlib libraries can be used to read data 
import pandas as pd # Pandas library can be used to create dataframes.
import matplotlib.pyplot as plt # matplotlib is used to plot graphs
import seaborn as sns
from scipy import stats # scipy and seaborn are needed for statistical analysis 
```
## II: Reading in and Processing the data 
* Pandas can be used to read in csv data.
```python
path = Path('data/northern_stage') # The variable 'path' stores the path named 'data/northern_stage'
electric = pd.read_csv(path/"electric.csv") # Use pd.read_csv to read the csv file into the variable 'electric'
```
* Check the data frame created:
```python
electric # Type in the variable directly can preview the data frame created 
electric.head()
electric.tail()# Preview the first or last 5 lines of the sheet
print(electric.columns.tolist()) # print the ' electric' to list form 
```
* Set the data  numerical form:
```python 
pd.set_option('display.float_format',lambda x: '%.2f' % x) # Set the format for display in float number
electric.describe() # Get the brief description of the electric 
```
* Set the date form:
```python
electric['Date'] = pd.to_datetime(electric['Date']) # Use pd.to_datetime to change the 'Date' column to the proper format (YY-MM-DD)

```
* Sort the dataframes:
```python 
electric = electric.sort_values(by='Date',ascending = False) # Sort the 'electric' by 'date' in ascending (or default descending )
```
* Merge the data in one data frame
```python 
df = pd.merge(gas, electric, suffixes = ("_gas", "_electric"), on="Date", how="outer")
# Use pd.merge () to store a new 'df' variable, merge the dataframes 'gas' and 'electric', parameter 'on=" "' denote the same (keep) part, suffixes("_x","_y") means add marks at the end of the same column from different dataframe, how ='' means union from each 
df = pd.merge( # merge the previous 'df' and an 'renamed' water 
    df,
    water.rename( 
        columns={col: col + "_water" for col in water.columns if col != "Date"}
    ),
    # use the 'DataFrame.rename' function to modify the dataframe 'water', 'columns='can be used to add '_water' to the old dataframe except 'Date' column
    on="Date",
    how="outer",
)

```
## III: Visualizing the Data 
### 1: Plotting a histogram 
* We use Pandas ' plot.hist function to plot the histogram:
```python 
electric.Unit.plot.hist(figsize=(8,8), color="orange", ec="white", bins=range(0,300000,1000)) # Use the function to plot 
plt.title('title')
plt.xlabel('X')
plt.ylabel('Y') # Set axis labels
plt.xlm(0,30000) # Set the x-lim
plt.show() # show the plot 

```
* Use the diff() function to calculate difference and create new column to store the data 
```python 
electric['reading_gaps']=electric.Date.diff().dt.total_seconds().divide(24*3600)
#Create a new column 'reading_gaps' store the gaps of date , use 'dt.total_seconds()' change the date form to seconds
```
* Use divide() create the consumption ratio with time:
```python
electric['cost_per_unit'] = electric['Calculated Cost'].divide(electric['Unit'])
```
### 2: Visualizing time series data 
* Use DataFrame.plot() to plot data with time:
```python
electric.plot(x='Date', y='Reading', figsize=(8,8))
plt.xlim('2010-03-01','2020-03-20')
# Set the date limit of x
plt.show()
```
### 3: Visualizing using Bar charts:
* Using bar charts to visualizing the categorical and numerical data 
```python
ax = df.groupby(df.Date.dt.month)[['Unit_gas', 'Unit_electric']].mean().plot.bar(figsize=(8,8))
# Define a new DataFrame to store, use groupby() to select the with data with group 'month' (using dt.month to pick 'month' in date), use '.mean()' to find the mean value.
ax.set_title('')
ax.set_xlabel()
ax.set_ylabel()
# Use DataFrame.set_title to set the title
```
### 4: Correlations in data 
* Using corr function to get the correlation:
```python
electric.corr()
```
* Visualizing the correlation:
```python
sns.set(rc={"figure.figsize":(12, 8)})
# sns for 'seaborn', '.set' can set the layout. 
slope, intercept, r_value, p_value, std_err = stats.linregress(electric['Unit'], electric['Carbon'])
# stats.linregress() can be use to calculate the slope, intercept and the r_value 
```
```cpp
//Test for git
# include<stdio.h>
int main()
{
    printf("%s","Test");
    return 0;
}
```





