# Digital-Signal-Processing--FIR-LOW-PASS-FILTER-DESIGN
## AIM:
To generate design of low pass FIR digital filter using Window.
## Software Required:
MAT LAB R2012.
## Algorithm:
Step 1: Open MATLAB and Write the program.

Step 2: Read the values of cut off frequency wc.

Step 2: Read the values of Order of the filter N.

Step 3: Find out the desired impulse response of the Low Pass filter Coefficient.

Step 4: Find out the windowing sequence.

Step 5: Plot the magnitude spectrum with x-label and y-label with suitable title.

Step 6: Terminate the program.

## PROGRAM: 
clc; % clear screen
 clear all; % clear screen
 close all; % close all figure windows
wc=input('enter the value of cut off frequency'); 
N=input('enter the value of filter'); 
alpha=(N-1)/2; 
eps=0.001; 
%Low Pass Filter Coefficient
n=0:1:N-1; 
hd=sin(wc*(n-alpha+eps))./(pi*(n-alpha+eps))
%Hamming Window Sequence 
n=0:1:N-1; 
wh=0.54-0.46*cos((2*pi*n)/(N-1)) 
hn=hd.*wh 
% Plot the Low Pass Filter with Hamming Window Technique
w=0:0.01:pi; 
h=freqz(hn,1,w); 
plot(w/pi,abs(h),'ms');
## OUTPUT:
![WhatsApp Image 2025-10-30 at 13 09 00_c0d547d1](https://github.com/user-attachments/assets/93a9fd9f-8e60-4a54-86c4-951e201c2213)


## RESULT:
![WhatsApp Image 2025-11-28 at 21 36 43_0f8394a4](https://github.com/user-attachments/assets/21127e74-0354-46ac-9fdb-76a92dcc1d0f)

