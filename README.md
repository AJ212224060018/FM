# EXP NO: 4 GENERATION AND DETECTION OF FM

### Aim:

To generate and detect the frequency modulation and demodulation u s i n g S C I L A B and to calculate modulation index of FM.

### Equiptments Required:

• Computer with i3 Processor
• SCI LAB

### Theory:

Frequency modulation is a type of modulation in which the frequency of the high frequency (carrier) is varied in accordance with the instantaneous value of the modulating signal. FREQUENCY DEVIATION f and MODULATION INDEX m f : The frequency deviation f represents the maximum shift between the modulatedsignal frequency, over and under the frequency of the carrier.

We define modulation index m f the ratio between f and the modulating frequency m= f / fm

### Frequency Modulation Generation: 
The circuits used to generate a frequency modulation must vary the frequency of a high frequency signal (carrier) as function of the amplitude of a low frequency signal (modulating signal). In practice there are two main methods used to generate FM.

Note: Keep all the switch faults in off position

### Algorithm:

#### Define Parameters: 
  • Fs: Sampling frequency. 
  • T: Duration of the signal. 
  • Fc: Carrier frequency. 
  • Fm: Frequency of the modulating signal. 
  • Beta: Modulation index, which controls the extent of frequency deviation.

#### Generate Signals: 
  • modulating_signal: Sinusoidal signal used for modulation. 
  • carrier_signal: The high-frequency carrier signal. 
  • modulated_signal: FM modulated signal calculated by varying the carrier frequency according to the modulating signal.

#### FM Modulation: 
  • Modulated_signal is obtained by modulating the carrier signal with the modulating signal.

#### FM Demodulation: 
  • Differentiation: Computes the derivative of the modulated signal to extract frequency variations. 
  • Envelope Detection: Takes the absolute value to retrieve the envelope of the signal. 
  • Low-pass Filtering: Applies a Butterworth low-pass filter to smooth the envelope and recover the original modulating signal.

#### Visualization: 
  • Plots the modulating signal, carrier signal, FM modulated signal, and demodulated signal for analysis.

### Procedure:

• Refer Algorithms and write code for the experiment. 
• Open SCILAB in System 
• Type your code in New Editor 
• Save the file 
• Execute the code 
• If any Error, correct it in code and execute again

### Model Graph:

<img width="410" height="293" alt="image" src="https://github.com/user-attachments/assets/523128c9-f936-43d0-b7fb-04a2bcaf7efb" />

### Program:
~~~
Am=10.96;
Ac=17.536;
fm=975;
fc=9750;
fs=97500;
t=0:1/fs:2/fm;
b=3.73;
em=Am*cos(2*3.14*fm*t);
subplot(3,1,1);
plot(t,em);
ec=Ac*cos(2*3.14*fc*t);
subplot(3,1,2);
plot(t,ec);
efm=Ac*cos(2*3.14*fc*t+b*sin(2*3.14*fm*t));
subplot(3,1,3);
plot(t,efm);
~~~
### Output Waveform:

<img width="760" height="721" alt="image" src="https://github.com/user-attachments/assets/103b8980-0443-487e-8a70-05132aedb7f3" />

### Tabulation:


### Calculation:

• ma (Theory) = am/ac = 2046.48
• ma(Practical) = (Emax-Emin)/(Emax+Emin) = 4.96

### Result:
Thus the amplitude modulation and demodulation is experimentally done and the output is verified.
