# **The Time Vector in the Fourier Transform** 🍌⏱️  

The **time vector** plays a critical role in the Fourier Transform, as it defines how a signal is sampled or observed in the **time domain** before being transformed to the **frequency domain**. Understanding the time vector is essential for accurate signal analysis.

---

## **1. What is the "Time Vector" in the Fourier Transform?**

The **time vector** refers to the sequence of discrete time points \( t_n \) at which a signal \( x(t) \) is sampled or evaluated.

- In the **Continuous Fourier Transform (CFT)**, the time variable \( t \) is continuous, and the signal \( x(t) \) exists for all \( t \in (-\infty, \infty) \).  
- In the **Discrete Fourier Transform (DFT)**, the time is represented as a **finite set of discrete points**.  

For the DFT, the time vector is defined as:

\[
t_n = n \cdot T_s, \quad n = 0, 1, ..., N-1
\]

Where:  
- \( t_n \): Discrete time instants.  
- \( T_s \): Sampling interval (the time between consecutive samples).  
- \( N \): Total number of samples.  

---

## **2. Relationship Between Time and Frequency**

The Fourier Transform reveals a **duality** between the time and frequency domains:

- A **slow phenomenon** in the time domain corresponds to a **narrow band** in the frequency domain.  
- A **fast phenomenon** in the time domain corresponds to a **broad band** in the frequency domain.  

This relationship highlights that improving **time resolution** reduces the **frequency resolution**, and vice versa.

---

## **3. The Time Vector in the Discrete Fourier Transform (DFT)**

In the DFT, the time is sampled at regular intervals \( T_s \), and the total duration of the signal is \( T_{\text{total}} \):

\[
T_{\text{total}} = N \cdot T_s
\]

The sampling frequency \( f_s \) (samples per second) is the inverse of the sampling interval:

\[
f_s = \frac{1}{T_s}
\]

**Example**:  
If \( T_s = 0.1 \, \text{s} \) (sample every 0.1 seconds) and \( N = 10 \), the time vector is:

\[
t = [0, 0.1, 0.2, 0.3, 0.4, 0.5, 0.6, 0.7, 0.8, 0.9] \, \text{s}
\]

---

## **4. Temporal and Spectral Resolution**

The time vector influences the **frequency resolution** in the DFT. The spectral resolution (\( \Delta f \)) is determined by the total duration of the signal:

\[
\Delta f = \frac{1}{T_{\text{total}}} = \frac{f_s}{N}
\]

- To achieve **better frequency resolution**, you need a **longer time vector** (larger \( N \)).  
- In other words, the longer you observe the signal, the finer the frequency details you can resolve.

---

## **5. Python Practical Example of the Time Vector**

Let's generate a sampled signal with a sampling frequency of \( f_s = 100 \, \text{Hz} \) over 1 second. Here's an example in Python:

```python
import numpy as np
import matplotlib.pyplot as plt

# Parameters
fs = 100  # Sampling frequency (Hz)
T = 1     # Total duration (s)
N = fs * T  # Total number of samples

# Time vector
t = np.linspace(0, T, N, endpoint=False)

# Signal: Combination of two sinusoids
f1, f2 = 5, 20  # Frequencies in Hz
x = np.sin(2 * np.pi * f1 * t) + np.sin(2 * np.pi * f2 * t)

# Plot the signal in the time domain
plt.plot(t, x)
plt.title("Signal in the Time Domain")
plt.xlabel("Time [s]")
plt.ylabel("Amplitude")
plt.grid()
plt.show()

```


## ** 6.MATLAB Practical Example of the Time Vector**

```matlab
% Parameters
fs = 100;          % Sampling frequency (Hz)
T = 1;             % Total duration (s)
N = fs * T;        % Total number of samples
t = linspace(0, T, N);  % Time vector

% Signal: Combination of two sine waves
f1 = 5;            % Frequency 1 (Hz)
f2 = 20;           % Frequency 2 (Hz)
signal = sin(2*pi*f1*t) + sin(2*pi*f2*t);

% Compute the Discrete Fourier Transform (DFT)
X = fft(signal);        % Perform the FFT
frequencies = (0:N-1)*(fs/N); % Frequency vector

% Compute the magnitude spectrum
X_magnitude = abs(X) / N;

% Plot the signal in the time domain
subplot(2,1,1);
plot(t, signal);
title('Signal in the Time Domain');
xlabel('Time [s]');
ylabel('Amplitude');
grid on;

% Plot the magnitude spectrum in the frequency domain
subplot(2,1,2);
plot(frequencies, X_magnitude);
title('Magnitude Spectrum of the Signal');
xlabel('Frequency [Hz]');
ylabel('Magnitude');
grid on;
```
