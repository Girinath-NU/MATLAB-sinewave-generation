# MATLAB 1 Hz Sine Wave Plot

## Overview
This MATLAB script generates and plots a **1 Hz sine wave** over a duration of 5 seconds. It also performs a **Fast Fourier Transform (FFT)** to visualize the sine wave in the frequency domain.

## Code Explanation
- **Time Vector (`t`)**: Defined from 0 to 5 seconds with a step size of 0.01 seconds.
- **Sine Wave (`y`)**: Generated using the formula:
  
  \[ y = \sin(2 \pi f t) \]
  
  where \( f = 1 \) Hz (one complete cycle per second).
- **Plotting (Time Domain)**: The `plot()` function is used to display the sine wave.
- **FFT (Frequency Domain Analysis)**:
  - Computes the Discrete Fourier Transform (DFT) using `fft()`.
  - Displays the magnitude spectrum to confirm the **1 Hz** frequency.

## MATLAB Code
```matlab
% Define parameters
fs = 100; % Sampling frequency (Hz)
t = 0:1/fs:5; % Time vector (5 seconds duration)

% Generate sine wave with 1 Hz frequency
y = sin(2 * pi * 1 * t);

% Plot the sine wave in the time domain
figure;
subplot(2,1,1);
plot(t, y);
xlabel('Time (s)');
ylabel('Amplitude');
title('1 Hz Sine Wave (Time Domain)');
grid on;

% Compute FFT
N = length(y); % Number of samples
Y = fft(y); % Compute FFT
f = (0:N-1)*(fs/N); % Frequency vector

% Plot magnitude spectrum
subplot(2,1,2);
plot(f(1:N/2), abs(Y(1:N/2))*2/N); % Single-sided amplitude spectrum
xlabel('Frequency (Hz)');
ylabel('Magnitude');
title('Frequency Domain Representation (FFT)');
grid on;
```

## Output
Running this script in MATLAB produces:
1. **Time Domain Plot**: A smooth 1 Hz sine wave.
2. **Frequency Domain Plot**: A peak at **1 Hz**, confirming the sine wave’s frequency.

## Usage
1. Open MATLAB.
2. Copy and paste the script into a new script file (e.g., `sine_wave.m`).
3. Run the script to visualize the **1 Hz sine wave** in both time and frequency domains.

## License
This project is open-source under the MIT License. Feel free to modify and use it as needed!

---
**Author:** Your Name

