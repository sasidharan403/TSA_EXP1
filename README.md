# Ex.No: 01A PLOT A TIME SERIES DATA

## Developed by :A.SASI DHARAN
## Register No : 212221240049
## Date :

# AIM:
To Develop a python program to Plot a time series data temperature.
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:
~~~
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("DailyDelhiClimateTrain.csv",parse_dates=["date"],index_col="date")
df.head()
mean=df["meantemp"].resample('M').mean().plot(kind='line')
plt.xlabel("Month")
plt.ylabel("Temperature")
plt.show()
~~~
# OUTPUT:



![image](https://github.com/user-attachments/assets/961c4665-76ab-4ba7-8c54-80e102f24a8f)



# RESULT:
Thus we have created the python code for plotting the time series of given data.
