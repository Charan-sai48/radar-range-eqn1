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
lambda = 0.05;      
sigma  = 2;         

Pt_vals = 0.5:0.5:20;   
Gt_const = 20;          
Pm_const = 1e-14;       

Rmax_Pt = ((Pt_vals .* Gt_const.^2 .* lambda.^2 .* sigma) ./ ((4*%pi)^3 .* Pm_const)).^(1/4);

Gt_vals = 5:2:100;      
Pt_const = 3;           
Pm_const = 1e-14;       

Rmax_Gt = ((Pt_const .* Gt_vals.^2 .* lambda.^2 .* sigma) ./ ((4*%pi)^3 .* Pm_const)).^(1/4);

Pm_vals = logspace(-14, -9, 50);  
Pt_const = 2;          
Gt_const = 25;         

Rmax_Pm = ((Pt_const .* Gt_const.^2 .* lambda.^2 .* sigma) ./ ((4*%pi)^3 .* Pm_vals)).^(1/4);

subplot(3,1,1);
plot(Pt_vals, Rmax_Pt, 'r', 'LineWidth', 2);

subplot(3,1,2);
plot(Gt_vals, Rmax_Gt, 'g', 'LineWidth', 2);

subplot(3,1,3);
plot(Pm_vals, Rmax_Pm, 'b', 'LineWidth', 2);
```

# Output:
<img width="760" height="623" alt="image" src="https://github.com/user-attachments/assets/5f95071f-fdbe-44fe-8d5b-5cd2c7f8fbef" />


# Tabulation:

![WhatsApp Image 2025-11-26 at 3 47 22 PM (1)](https://github.com/user-attachments/assets/4e1833de-7e64-4dd6-933b-b6d69edcccee)


# Result :
Thus the maximum range of a radar system using the Radar Range Equation is verified through a Python program.
