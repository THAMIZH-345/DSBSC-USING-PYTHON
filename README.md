
# DSBSC-USING-PYTHON

## AIM:

To implement and analyze DSBSC using Python's NumPy and Matplotlib libraries. 

## EQUIPMENTS REQUIRED

1.	Software: Python with NumPy and Matplotlib libraries
2.	Hardware: Personal Computer


## Algorithm:

1.	Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
5.	Generate DSBSC Signal: Apply the DSBSC formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.


## Program
```asm
import numpy as np
import matplotlib.pyplot as plt
Am = 4.9
Ac = 9.8
fm = 417
fc = 4170
fs = 41700
t = np.arange(0,2/fm,1/fs)
m= Am*np.cos(2*3.14*fm*t)
plt.subplot(3,1,1)
plt.plot(t,m)
c=Ac*np.cos(2*3.14*fc*t)
plt.subplot(3,1,2)
plt.plot(t,c)
s1=(Ac+m)*np.cos(2*3.14*fc*t)
s2=(Ac-m)*np.cos(2*3.14*fc*t)
s=s1-s2
plt.subplot(3,1,3)
plt.plot(t,s)
```

## Output Graph

<img width="711" height="512" alt="image" src="https://github.com/user-attachments/assets/9f439d40-20fc-4895-8a17-2ca2f5315c93" />

## Tablular Column

<img width="1200" height="1600" alt="image" src="https://github.com/user-attachments/assets/09b4dbe3-d8c3-4cd6-8e81-e6e222952a93" />

## Result

Thus the DSB-SC-AM Modulation is generated using python.

