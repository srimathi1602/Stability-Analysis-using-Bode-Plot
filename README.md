# Stability-Analysis-using-Bode-Plot
## Aim:
To analyse the stability of the system having open loop transfer function, G(S)=1/(S(1+0.5S)(1+0.1S)) using bode plot and verify it using MATLAB. 
## Apparatus Required:
Computer with MATLAB software

## Theory:

![WhatsApp Image 2025-11-27 at 21 36 01_0718bd36](https://github.com/user-attachments/assets/a234b5ab-c0b9-4798-82c9-8adddd104ba5)
![WhatsApp Image 2025-11-27 at 21 36 01_25ff6469](https://github.com/user-attachments/assets/16aaae3f-0ed1-4b55-ad12-73603c2c84a0)
![WhatsApp Image 2025-11-27 at 21 36 01_8b24bd9e](https://github.com/user-attachments/assets/88eec403-5f05-4f7d-889c-927eede97296)
![WhatsApp Image 2025-11-27 at 21 36 02_5d70602b](https://github.com/user-attachments/assets/fd4dc27d-6419-4c4b-85fb-b3b2b953b0c6)


## Procedure:
	Open MATLAB software
	Open a new script file.
	Type the program.
	Save and Execute the program.
	Determine the gain crossover frequency, phase cross over frequency, gain margin and phase margin.
	Also determine the stability.

## Program: 
```
num=1
den=[0.05 0.6 1 0]
sys=tf(num,den)
bode(sys)
grid on
[Gm Pm Wpc Wgc]=margin(sys)
if(Wpc>Wgc)
    disp('stable')
elseif(Wpc == Wgc)
    disp('marginally stable')
else
    disp('unstable')
end
```
## Output:
<img width="828" height="402" alt="Screenshot 2025-11-24 175805" src="https://github.com/user-attachments/assets/21394774-a778-4e2f-a145-eda0ba51d618" />


## Result:
Thus the bode plot for the given transfer function was drawn and verified using MATLAB.
```
Gain margin = 12
Phase Margin = 60.4231
Gain crossover frequency = 0.9070
Phase crossover frequency = 4.4721
The system is stable
```
