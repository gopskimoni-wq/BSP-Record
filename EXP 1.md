## EXP NO: 01	TO PLOT THE FFT OF A SEQUENCE.
## DATE : 
# AIM:
To plot FFT of the given sequence x(n)= {2,1,2,1,1,1,2,1,2} and sketch the magnitude and phase spectrum using MATLAB.
# REQUIREMENTS:
	MATLAB software
	Computer
# Theory
The Fast Fourier Transform (FFT) is an efficient algorithm to compute the Discrete Fourier Transform (DFT) of a sequence.
For a sequence x(n), the DFT is defined as:
 
The magnitude spectrum is given by:
 
The phase spectrum is given by:
 
# ALGORITHM:
Define the input sequence x(n).
	Determine the length NNN of the sequence.
	Apply the fft() function in MATLAB to compute the DFT.
	Compute magnitude and phase using abs() and angle() functions.
	Plot the input sequence, magnitude spectrum, and phase spectrum using subplots.
## MATLAB CODE
clc;
clear;
close all;

% Step 1: Define input sequence
x = [2 1 2 1 1 1 2 1 2];	
N = length(x);

% Step 2: Compute FFT
X = fft(x);

% Step 3: Compute magnitude and phase
magX = abs(X);
phaseX = angle(X);

% Step 4: Plot results
subplot(3,1,1);
stem(0:N-1, x, 'filled');
title('Input Sequence x(n)');
xlabel('n');
ylabel('Amplitude');
grid on;

subplot(3,1,2);
stem(0:N-1, magX, 'filled');
title('Magnitude Spectrum');
xlabel('Frequency Index k');
ylabel('|X(k)|');
grid on;

subplot(3,1,3);
stem(0:N-1, phaseX, 'filled');
title('Phase Spectrum');
xlabel('Frequency Index k');
ylabel('Phase (radians)');
grid on;

## sample OUTPUT
<img width="698" height="419" alt="image" src="https://github.com/user-attachments/assets/2008c38c-f24c-4381-b7ef-240f894ad74c" />



## your output 


## RESULT:
Thus,the FFT of the sequence was plotted using MATLAB.

