# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 18-03-25

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:
```
DEVELOPED BY: KUKKADAPU CHARAN TEJ
REGISTER NUMBER:212224040167
```


```py

from matplotlib import pyplot as plt
import pandas as pd
df=pd.read_csv("/content/AirPassengers.csv")
# df=pd.read_csv("/content/test.csv",parse_dates=["date"],index_col="date")
df.head()
df['Month']=pd.to_datetime(df['Month'])
df.dtypes
df.set_index('Month',inplace=True)
df_resampled = df['#Passengers'].resample('D').interpolate()
df_resampled.plot(kind='line',label='Total Sales', color='black')
plt.title('Time Series Plot of Number of passengers ecah day')
plt.xlabel('Day')
plt.ylabel('Number of passengers')
plt.legend()
plt.grid(True)
plt.show()
```
# OUTPUT:
![Screenshot 2025-03-18 082136](https://github.com/user-attachments/assets/b00dddb8-430f-4490-88e2-fcb1ff88755c)

# RESULT:
Thus we have created the python code for plotting the time series of given data.
