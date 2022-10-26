---
title: Pandas CheatSheet
description: The most commonly used pandas commands are given here.
created: 2022-10-24
---

## Table of Contents

- [Pandas CheatSheet for Developers](#pandas-cheatsheet-for-developers)
  - [Introduction-What-is-Pandas?](#introduction-what-is-pandas)
  - [Key and Imports](#key-and-imports)
  - [Importing Data](#importing-data)
  - [Exporting data](#exporting-data)
  - [Create Test objects](#create-test-objects)
  - [Viewing/Inspecting Data](#viewinginspecting-data)
  - [Selection](#selection)
  - [Data cleaning](#data-cleaning)
  - [Filter, Sort, and Groupby](#filter-sort-and-groupby)
  - [Join/Combine](#joincombine)
  - [Statistics](#statistics)
  - [Data Visualization with dataframe](#data-visualization-with-dataframe)
    - [Terminology And Definitions](#terminology-and-definitions)
    - [Type of plots](#type-of-plots)


# Pandas CheatSheet for Developers

## Introduction-What-is-Pandas?

> Pandas can be used as the **most important Python** package for **Data Science**. It helps to provide a lot of functions that deal with the data in easier way. It's **fast, flexible, and expressive data structures** are designed to make real-world data analysis.
> Pandas Cheat Sheet is a quick guide through the basics of Pandas that you will need to get started on wrangling your data with Python. If you want to begin your data science journey with Pandas, you can use it as a handy reference to deal with the data easily.

This cheat sheet will guide through the basics of the Pandas library from the data structure to I/O, selection, sorting and ranking, etc.

**[🔼Back to Top](#table-of-contents)**

## Key and Imports

> We use following shorthand in the cheat sheet:

|Command | description|
|----------|-------------|
|`pd`|import pandas library| 
|`df` | Refers to any Pandas Dataframe object.|
|`s` | Refers to any Pandas Series object.|

> You can use the following imports to get started:

**[🔼Back to Top](#table-of-contents)**

## Importing Data

|Command | description|
|---------|-------------|
|`pd.read_csv(filename)` | It read the data from CSV file.|
|`pd.read_table(filename)` | It is used to read the data from delimited text file.|
|`pd.read_excel(filename)` | It read the data from an Excel file.|
|`pd.read_sql(query,connection _object)`| It read the data from a SQL table/database.|
|`pd.read_json(json _string)` | It read the data from a JSON formatted string, URL or file.|
|`pd.read_html(url)` | It parses an html URL, string or the file and extract the tables to a list of dataframes.|
|`pd.read_clipboard()` | It takes the contents of clipboard and passes it to the read_table() function.|
|`pd.DataFrame(dict)` | From the dict, keys for the columns names, values for the data as lists.|

**[🔼Back to Top](#table-of-contents)**

## Exporting data

|Command | description|
|-------------|----------|
|`df.to_csv(filename)`| It writes to a CSV file.|
|`df.to_excel(filename)`| It writes to an Excel file.|
|`df.to_sql(table_name, connection_object)`| It writes to a SQL table.|
|`df.to_json(filename)` | It write to a file in JSON format.|

**[🔼Back to Top](#table-of-contents)**

## Create Test objects

> It is useful for testing the code segments.

|Command | description|
|-------------|----------|
|`pd.DataFrame(np.random.rand(7,18))`| Refers to 18 columns and 7 rows of random floats.|
|`pd.Series(my_list)`| It creates a Series from an iterable my_list.|
|`df.index= pd.date_range('1940/1/20', periods=df.shape[0])`|It adds the date index.|

**[🔼Back to Top](#table-of-contents)**

## Viewing/Inspecting Data

|Command | description|
|-------------|----------|
|`df.head(n)`| It returns first n rows of the DataFrame.By default it will return first 5 rows|
|`df.tail(n)` | It returns last n rows of the DataFrame.By default it will return last 5 rows|
|`df.shape` | It returns number of rows and columns.|
|`df.info()`| It returns index, Datatype, and memory information.|
|`s.value_counts(dropna=False)`| It views unique values and counts.|
|`df.apply(pd.Series.value_counts)`| It refers to the unique values and counts for all the columns.|

**[🔼Back to Top](#table-of-contents)**

## Selection

|Command | description|
|-------------|----------|
|`df[col1]` | It returns column with the label col as Series.|
|`df[[col1, col2]]`| It returns columns as a new DataFrame.|
|`s.iloc[0]` | It select by the position.|
|`s.loc['index_one']` | It select by the index.|
|`df.iloc[0,:]`| It returns first row.|
|`df.iloc[0,0]` | It returns the first element of first column.|

**[🔼Back to Top](#table-of-contents)**

## Data cleaning

|Command | description|
|-------------|----------|
|`df.columns` = ['a','b','c'] | It rename the columns.|
|`pd.isnull()` | It checks for the null values and returns the Boolean array.|
|`pd.notnull()` | It is opposite of pd.isnull().|
|`df.dropna()`|It drops all the rows that contain the null values.|
|`df.dropna(axis= 1)`| It drops all the columns that contain null values.|
|`df.dropna(axis=1,thresh=n)`| It drops all the rows that have less than n non null values.|
|`df.fillna(x)`| It replaces all null values with x.|
|`s.fillna(s.mean())`| It replaces all the null values with the mean(the mean can be replaced with almost any function from the statistics module).|
|`s.astype(float)`| It converts the datatype of series to float.|
|`s.replace(1, 'one')`| It replaces all the values equal to 1 with 'one'.|
|`s.replace([1,3],[ 'one', 'three'])`|It replaces all 1 with 'one' and 3 with 'three'.|
|`df.rename(columns=lambda x: x+1)`|It rename mass of the columns.|
|`df.rename(columns={'old_name': 'new_ name'})`| It consist selective renaming.|
|`df.set_index('column_one')`| Used for changing the index.|
|`df.rename(index=lambda x: x+1)`| It rename mass of the index.|

**[🔼Back to Top](#table-of-contents)**

## Filter, Sort, and Groupby

|Command | description|
|-------------|----------|
|`df[df[col] > 0.5]` | Returns the rows where column col is greater than 0.5|
|`df[(df[col] > 0.5) & (df[col] < 0.7)]`| Returns the rows where 0.7 > col > 0.5|
|`df.sort_values(col1)` | It sorts the values by col1 in ascending order.|
|`df.sort_values(col2,ascending=False)` | It sorts the values by col2 in descending order.|
|`df.sort_values([col1,col2],ascending=[True,False])` | It sort the values by col1 in ascending order and col2 in descending order.|
|`df.groupby(col1)`| Returns a groupby object for the values from one column.|
|`df.groupby([col1,col2])`| Returns a groupby object for values from multiple columns.|
|`df.groupby(col1)[col2])` | Returns mean of the values in col2, grouped by the values in col1.|
|`df.pivot_table(index=col1,values=[col2,col3],aggfunc=mean)` | It creates the pivot table that groups by col1 and calculate mean of col2 and col3.|
|`df.groupby(col1).agg(np.mean`) | It calculates the average across all the columns for every unique col1 group.|
|`df.apply(np.mean)` | Its task is to apply the function np.mean() across each column.|
|`nf.apply(np.max,axis=1)`|Its task is to apply the function np.max() across each row.|

**[🔼Back to Top](#table-of-contents)**

## Join/Combine

|Command | description|
|-------------|----------|
|`df1.append(df2)`| Its task is to add the rows in df1 to the end of df2(columns should be identical).|
|`pd.concat([df1, df2], axis=1)`| Its task is to add the columns in df1 to the end of df2(rows should be identical).|
|`df1.join(df2,on=col1,how='inner')`| SQL-style join the columns in df1 with the columns on df2 where the rows for col have identical values, 'how' can be of 'left', 'right', 'outer', 'inner'.|

**[🔼Back to Top](#table-of-contents)**

## Statistics

> The statistics functions can be applied to a Series, which are as follows:

|Command | description|
|-------------|----------|
|`df.describe()`| It returns the summary statistics for the numerical columns.|
|`df.mean()` | It returns the mean of all the columns.|
|`df.corr()` | It returns the correlation between the columns in the dataframe.|
|`df.count()`| It returns the count of all the non-null values in each dataframe column.|
|`df.max()`| It returns the highest value from each of the columns.|
|`df.min()`| It returns the lowest value from each of the columns.|
|`df.median()`| It returns the median from each of the columns.|
|`df.std()`| It returns the standard deviation from each of the columns.|

**[🔼Back to Top](#table-of-contents)**

## Data Visualization with dataframe

### Terminology And Definitions

|data| DataFrame|
|--------|------|
|`x`| label or position, default None|
|`y` | label, position or list of label, positions, default None Allows plotting of one column versus another|
|`ax `| matplotlib axes object, default None|
|`subplots`| boolean, default False Make separate subplots for each column|
|`sharex `| boolean, default True if ax is None else False. Be aware, that passing in both an ax and sharex=True will alter all x axis labels for all axis in a figure!|
|`sharey`| boolean, default False In case subplots=True, share y axis and set some y axis labels to invisible|
|`layout`|tuple (optional) (rows, columns) for the layout of subplots|
|`figsize`| a tuple (width, height) in inches|
|`use_index `| boolean, default True. Use index as ticks for x axis|
|`title `| string or list. Title to use for the plot. If a string is passed, print the string at the top of the figure. If a list is passed and subplots is True, print each item in the list above the corresponding subplot.|
|`grid `| boolean, default None (matlab style default). Axis grid lines|
|`legend`| False/True/’reverse’. Place legend on axis subplots|
|`style `| list or dict. Matplotlib line style per column|
|`logx `| boolean, default False. Use log scaling on x axis|
|`logy `| boolean, default False. Use log scaling on y axis|
|`loglog `| boolean, default False. Use log scaling on both x and y axes|
|`xticks `| sequence. Values to use for the xticks|
|`yticks `| sequence. Values to use for the yticks|
|`xlim `| 2-tuple/list|
|`ylim `| 2-tuple/list|
|`rot `| int, default None. Rotation for ticks (xticks for vertical, yticks for horizontal plots)|
|`fontsize `| int, default None. Font size for xticks and yticks|
|`colormap `| str or matplotlib colormap object, default None. Colormap to select colors from. If string, load colormap with that name from matplotlib.|
|`colorbar `| boolean, optional. If True, plot colorbar (only relevant for ‘scatter’ and ‘hexbin’ plots)|
|`position `| float. Specify relative alignments for bar plot layout. From 0 (left/bottom-end) to 1 (right/top-end). Default is 0.5 (center)|
|`table `| boolean, Series or DataFrame, default False. If True, draw a table using the data in the DataFrame and the data will be transposed to meet matplotlib’s default layout. If a Series or DataFrame is passed, use passed data to draw a table.|
|`yerr `| DataFrame, Series, array-like, dict and str. See Plotting with Error Bars for detail.|
|`xerr `| same types as yerr.|
|`stacked `| boolean, default False in line and bar plots, and True in area plot. If True, create stacked plot.|
|`sort_columns `| boolean, default False. Sort column names to determine plot ordering|
|`secondary_y `| boolean or sequence, default False. Whether to plot on the secondary y-axis If a list/tuple, which columns to plot on secondary y-axis|
|`mark_right `| boolean, default True. When using a secondary_y axis, automatically mark the column labels with “(right)” in the legend|
|`kwds`|  keywords .Options to pass to matplotlib plotting method|
|`axes`|  matplotlib.axes.Axes or numpy.ndarray of them|

**[🔼Back to Top](#table-of-contents)**

### Type of plots

`Note it is a part of data Visualization`


|king|type|
|-----|-----|
|`‘line’ `| line plot (default)|
|`‘bar’ `| vertical bar plot|
|`‘barh’ `| horizontal bar plot|
|`‘hist’ `| histogram|
|`‘box’ `| boxplot|
|`‘kde’ `| Kernel Density Estimation plot|
|`‘density’ `| same as ‘kde’|
|`‘area’`| area plot|
|`‘pie’ `| pie plot|
|`‘scatter’ `| scatter plot|
|`‘hexbin’ `| hexbin plot|

**[🔼Back to Top](#table-of-contents)**
