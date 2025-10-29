# EVALUATION OF RADAR RANGE 
# Aim:
To calculate the maximum range of a radar system using the Radar Range Equation and verify the results through Python programming.

# Theory:
The Radar Range Equation is a fundamental formula used in radar system design to determine the maximum range at which a radar can detect a target. It is given by:

<img width="367" height="424" alt="Screenshot 2025-10-29 154151" src="https://github.com/user-attachments/assets/3958d1ea-e021-4629-96f7-65a3a177d555" />

# Procedure:
1.	Set Up the Python Environment: Ensure that Python is installed on your system. You can use Anaconda for managing Python packages and environments, or any other Python IDE of your choice.
2.	Import Necessary Libraries: Import the math library in Python.
3.	Define the Radar Range Equation Function: Create a function to calculate the maximum range using the Radar Range Equation.
4.	Input Parameters for the Radar System: Define the input parameters such as transmitted power, transmitter gain, receiver gain, radar frequency, radar cross section, and minimum detectable power.
5.	Calculate the Maximum Range: Use the function to calculate the maximum range of the radar.
6.	Execute the Program: Run the Python script to calculate and display the maximum range of the radar.

# Code:
```
c = 3e8;
f = 10e9;
lambda = c / f;
sigma = 1;
L = 1;

Pt = 1e3;
G = 30;
R = 1e3:100:50e3;
Pr1 = (Pt * (G^2) * (lambda^2) * sigma) ./ ((4*%pi)^3 * (R.^4) * L);
subplot(3,1,1);
plot(R/1000, 10*log10(Pr1));

Pt2 = 100:100:5000;
R2 = 20e3;
Pr2 = (Pt2 * (G^2) * (lambda^2) * sigma) ./ ((4*%pi)^3 * (R2^4) * L);
subplot(3,1,2);
plot(Pt2, 10*log10(Pr2));

G3 = 10:2:60;
R3 = 20e3;
Pr3 = (Pt * (G3.^2) * (lambda^2) * sigma) ./ ((4*%pi)^3 * (R3^4) * L);
subplot(3,1,3);
plot(G3, 10*log10(Pr3));
```

# Output:
<img width="756" height="626" alt="Screenshot 2025-10-22 155059" src="https://github.com/user-attachments/assets/b7794dfb-b014-483a-801b-ec173293f62e" />

# Tabulation:

# Result :
Thus the maximum range of a radar system using the Radar Range Equation is verified through a Python program.
