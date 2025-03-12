# MATLAB 1 Hz Sine Wave Plot

## Overview
This MATLAB script generates and plots a **1 Hz sine wave** over a duration of 5 seconds. The script utilizes the `sin()` function to create the wave and `plot()` to visualize it.

## Code Explanation
- **Time Vector (`t`)**: Defined from 0 to 5 seconds with a step size of 0.01 seconds.
- **Sine Wave (`y`)**: Generated using the formula:
  
  \[ y = \sin(2 \pi f t) \]
  
  where \( f = 1 \) Hz (one complete cycle per second).
- **Plotting**: The `plot()` function is used to display the sine wave, with appropriate labels and a grid.

## MATLAB Code
```matlab
% Define parameters
t = 0:0.01:5; % Time vector (5 seconds duration)

% Generate sine wave with 1 Hz frequency
y = sin(2 * pi * 1 * t);

% Plot the sine wave
figure;
plot(t, y);
xlabel('Time (s)');
ylabel('Amplitude');
title('1 Hz Sine Wave');
grid on;
```

## Output
Running this script in MATLAB produces a plot of a **1 Hz sine wave** with smooth oscillations over 5 seconds.

## Usage
1. Open MATLAB.
2. Copy and paste the script into a new script file (e.g., `sine_wave.m`).
3. Run the script to visualize the 1 Hz sine wave.

## License
This project is open-source under the MIT License. Feel free to modify and use it as needed!

---
**Author:** Your Name

