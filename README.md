# Ex.No: 01A PLOT A TIME SERIES DATA

## Developed by :A.SASI DHARAN
## Register No : 212221240049
## Date :

# AIM:
To Develop a python program to Plot a time series data on Global temperature
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:
~~~
import pandas as pd
import matplotlib.pyplot as plt
df = pd.read_csv('climate_data.csv')
df['dt'] = pd.to_datetime(df['dt'])
df.set_index('dt', inplace=True)
plt.figure(figsize=(12, 6))
plt.plot(df.index, df['AverageTemperature'], color='red', marker='o', linestyle='-') # Changed 'Temperature_Anomaly' to 'AverageTemperature'
plt.title('Global Temperature Anomalies Over Time')
plt.xlabel('Year')
plt.ylabel('Temperature Anomaly (°C)')
plt.grid(True)
plt.show()
~~~
# OUTPUT:

![image](https://github.com/user-attachments/assets/cec98d5d-8fe4-49ac-969d-aef94bcee11c)




# RESULT:
we have created the python code for plotting the time series of given data.
