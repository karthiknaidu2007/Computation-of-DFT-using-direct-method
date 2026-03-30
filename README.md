# EXPT 1: Computation-of-DFT-using-direct-method

## AIM
To perform and verify DFT using direct method by SCILAB.
## APPARATUS REQUIRED
PC installed with SCILAB
## PROGRAM 
### DFT DIRECT METHOD
```clc;
clear;
xn=[1 2 3 4 4 3 2 1];
n1=0:1:length(xn)-1;
subplot(3,1,1);
plot2d3(n1,xn);
xlabel('Time n');
ylabel('Amplitude xn');
title('Input Sequence');
j=sqrt(-1);
N=length(xn);
Xk=zeros(1,N);
    for k=0:N-1;
    for n=0:N-1;  
    Xk(k+1)=Xk(k+1)+xn(n+1)*exp((-j*2*%pi*k*n)/N);
    end
end
disp(Xk)
K1=0:1:length(Xk)-1;
magnitude=abs(Xk)
subplot(3,1,2);
plot2d3(K1,magnitude);
xlabel('frequency(Hz)');
ylabel('magnitude(gain)');
title('magnitude spectrum');
angle=atan(imag(Xk),real(Xk))
subplot(3,1,3);
plot2d3(K1,angle);
xlabel('frequency(Hz)');
ylabel('Phase');
title('Phase spectrum');
```
### CALCULATIONS:

<img width="984" height="1589" alt="image" src="https://github.com/user-attachments/assets/f48f0c16-249d-440b-be1c-c67c33560b1f" />
<img width="993" height="1600" alt="image" src="https://github.com/user-attachments/assets/1098c371-3b5d-4a50-9865-2ad1c0ff2096" />
<img width="992" height="1510" alt="image" src="https://github.com/user-attachments/assets/8577b37b-26c5-49a3-9297-c95005273601" />
<img width="959" height="1529" alt="image" src="https://github.com/user-attachments/assets/6c66fba0-61cb-4670-8d27-77dc7a788646" />
<img width="1523" height="671" alt="image" src="https://github.com/user-attachments/assets/cca8b998-9f02-49d5-8b7e-b10476c1ffa6" />
<img width="891" height="1471" alt="image" src="https://github.com/user-attachments/assets/a185b0b8-d014-4bee-88d5-20a82a3aff63" />

### SAMPLE OUTPUT:
<img width="1920" height="1200" alt="Screenshot 2026-02-09 090154" src="https://github.com/user-attachments/assets/364ea9d9-1c90-4dcb-b4cc-116c68248512" />


## RESULT:
Thus,  DFT using direct method for two given sequences were performed and its result was verified.
