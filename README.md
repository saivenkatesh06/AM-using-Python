# AM-using-Python

## Aim


To implement and analyze amplitude modulation (AM) using Python's NumPy and Matplotlib libraries. 

## Apparatus Required

1.	Software: Python with NumPy and Matplotlib libraries
2.	Hardware: Personal Computer
  
## Theory

Amplitude Modulation (AM) is a technique used in electronic communication, primarily for transmitting information via a radio carrier wave. The general form of an FM signal is:



## Algorithm


1.	Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
5.	Generate AM Signal: Apply the AM modulation formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

## Program

``
import numpy as np
import matplotlib.pyplot as plt
Am=5.6
fm=451
Ac=11.2
fc=4510
fs=45100
t=np.arange(0,2/fm,1/fs)
m = Am*np.cos(2*np.pi*fm*t)
c=Ac*np.cos(2*np.pi*fc*t)
s = (Ac+Am*np.cos(2*np.pi*fm*t))*np.cos(2*np.pi*fc*t)
plt.subplot(3,1,1)
plt.plot(t, m)
plt.subplot(3,1,2)
plt.plot(t,c)
plt.subplot(3,1,3)
plt.plot(t,s)
``

## Output Waveform

<img width="554" height="413" alt="image" src="https://github.com/user-attachments/assets/72ec5b4d-5e90-420d-bef8-4b3be5cabc15" />



## Tabular Column

<img width="1200" height="1600" alt="image" src="https://github.com/user-attachments/assets/13fefa2b-1695-4f9c-a5ca-99080f824122" />



## Result

The message signal, carrier signal, and amplitude modulated (AM) signal will be displayed in separate plots. The modulated signal will show amplitude variations corresponding to the amplitude of the message signal.
