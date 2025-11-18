# Stability-Analysis-using-Bode-Plot
## Aim:
To analyse the stability of the system having open loop transfer function, G(S)=1/(S(1+0.5S)(1+0.1S)) using bode plot and verify it using MATLAB. 
## Apparatus Required:
Computer with MATLAB software
## Theory:
![Image 2025-11-18 at 11 25 14 AM](https://github.com/user-attachments/assets/355a6ffb-9d98-469a-8f21-e8f76abad7a9)
![Image 2025-11-18 at 11 25 51 AM](https://github.com/user-attachments/assets/77852c27-4d44-472a-9d54-87191cad1b68)
## Procedure:
	Open MATLAB software
	Open a new script file.
	Type the program.
	Save and Execute the program.
	Determine the gain crossover frequency, phase cross over frequency, gain margin and phase margin.
	Also determine the stability.
## Program: 
	num=[1]
	den=[0.05 0.6 1 0]
	sys=tf(num,den)
	bode(sys)
	grid on;
	[Gm Pm Wpc Wgc]=margin(sys)
	GmindB=20*log10(Gm)
	if(Wpc > Wgc)
	    disp('stable')
	elseif(Wpc == Wgc)
	    disp('marginally stable')
	else
	    disp('unstable')
	end


## Output:
<img width="1918" height="1193" alt="image" src="https://github.com/user-attachments/assets/a490171e-c446-484d-99f2-9b3f4564ec39" />
## Result:
Thus the bode plot for the given transfer function was drawn and verified using MATLAB. <br>
Gain margin = 12 <br>
Phase Margin = 60.42 <br>
Gain crossover frequency = 0.9 rad/s<br>
Phase crossover frequency = 4.47 rad/s<br>
The system is stable
