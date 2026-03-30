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
![DFT-1](https://github.com/user-attachments/assets/0de39c89-ad4f-488a-a86a-1025ca6d9f2a)

![DFT-2](https://github.com/user-attachments/assets/aca83c89-db29-48f1-9fa7-77ba802fa496)
