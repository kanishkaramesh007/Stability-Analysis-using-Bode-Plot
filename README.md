# Stability-Analysis-using-Bode-Plot
## Aim:
To analyse the stability of the system having open loop transfer function, G(S)=1/(S(1+0.5S)(1+0.1S)) using bode plot and verify it using MATLAB. 
## Apparatus Required:
Computer with MATLAB software

## Theory:
![WhatsApp Image 2025-11-27 at 20 47 58_7da3efb1](https://github.com/user-attachments/assets/1539b4b2-f106-47fe-9344-a525aee2366c)
![WhatsApp Image 2025-11-27 at 20 48 30_635c803c](https://github.com/user-attachments/assets/aa2daa3e-5597-453e-af33-1ad0e090315b)
![WhatsApp Image 2025-11-27 at 20 48 58_65315e9c](https://github.com/user-attachments/assets/014313a9-b53e-44d4-8620-b81f1346f242)



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
<img width="702" height="629" alt="image" src="https://github.com/user-attachments/assets/1bcfe0b7-9084-447e-b972-1bd863380aeb" />


## Result:
Thus the bode plot for the given transfer function was drawn and verified using MATLAB. <br>
Gain margin = 12.0 <br>
Phase Margin =  60.42 <br>
Gain crossover frequency = 0.907<br>
Phase crossover frequency =  4.4721<br>
The system is stable
