# Ex.No:04   FIT ARMA MODEL FOR TIME SERIES
# Date: 16.03.2024
### AIM:
To implement ARMA model in python.
### ALGORITHM:
1. Import necessary libraries.
2. Set up matplotlib settings for figure size.
3. Define an ARMA(1,1) process with coefficients ar1 and ma1, and generate a sample of 1000

data points using the ArmaProcess class. Plot the generated time series and set the title and x-
axis limits.

4. Display the autocorrelation and partial autocorrelation plots for the ARMA(1,1) process using
plot_acf and plot_pacf.
5. Define an ARMA(2,2) process with coefficients ar2 and ma2, and generate a sample of 10000

data points using the ArmaProcess class. Plot the generated time series and set the title and x-
axis limits.

6. Display the autocorrelation and partial autocorrelation plots for the ARMA(2,2) process using
plot_acf and plot_pacf.
### PROGRAM:
```
NAME : YAMUNAASRI T S
REG NO : 212222240117
```
```
from pandas import read_csv
from pandas import datetime
from matplotlib import pyplot
from pandas.plotting import autocorrelation_plot
from pandas import DataFrame
from statsmodels.tsa.arima_model import ARIMA
from statsmodels.graphics.tsaplots import plot_acf, plot_pacf
from statsmodels.tsa.arima_process import ArmaProcess
import matplotlib.pyplot as plt
import numpy as np
import warnings
warnings.filterwarnings('ignore')
import matplotlib.pyplot as plt
import numpy as np

plt.rcParams['figure.figsize'] = [10, 7.5]

ar1 = np.array([1,0.33])
ma1 = np.array([1,0.9])
ARMA_1 = ArmaProcess(ar1,ma1).generate_sample(nsample = 1000)
plt.plot(ARMA_1)
plt.title('Simulated ARMA(1,1) Process')
plt.xlim([0, 200])
plt.show()
plot_acf(ARMA_1)
plot_pacf(ARMA_1)
ar2 = np.array([1, 0.33, 0.5])
ma2 = np.array([1, 0.9, 0.3])
ARMA_2 = ArmaProcess(ar2, ma2).generate_sample(nsample=10000)
plt.plot(ARMA_2)
plt.title('Simulated ARMA(2,2) Process')
plt.xlim([0, 200])
plt.show()
plot_acf(ARMA_2)
plot_pacf(ARMA_2)
```
### OUTPUT:
SIMULATED ARMA(1,1) PROCESS:
![image](https://github.com/Yamunaasri/TSA_EXP4/assets/115707860/6679cb56-21ab-431f-8e87-e3d5bc9762d1)

Partial Autocorrelation
![image](https://github.com/Yamunaasri/TSA_EXP4/assets/115707860/75a682bb-23e3-4d55-a178-dcba5549225d)

Autocorrelation
![image](https://github.com/Yamunaasri/TSA_EXP4/assets/115707860/0baf181f-f390-4f67-bba6-4b6d175cd9ad)

SIMULATED ARMA(2,2) PROCESS:
![image](https://github.com/Yamunaasri/TSA_EXP4/assets/115707860/429c1676-eaf8-412f-9f1f-961544bbe3f0)

Partial Autocorrelation
![image](https://github.com/Yamunaasri/TSA_EXP4/assets/115707860/1007b658-18d4-4330-ba2e-a1b9fe2a6507)

Autocorrelation
![image](https://github.com/Yamunaasri/TSA_EXP4/assets/115707860/748164ec-bf14-4365-b1ac-39042cca7668)

### RESULT:
Thus, a python program is created to fir ARMA Model successfully.
