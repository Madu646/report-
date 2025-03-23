# Linear Integrated Circuit
# Current Mirroring Experiment
# PART-A
## Aim

Design and Analyze Current mirror circuit as active load in amplifier circuit.
**Circuit Diagram:**
![image](https://github.com/user-attachments/assets/87414ce5-50cc-47d9-babf-2fd26144c1cb)


**Given** :

Vdd=1.8V.

P<=1mW.

Av>-10V/V.
It=P/Vdd.
It=Iref+Ix.
## DC Analysis:
# For mirror ratio 1:1:
 It=Iref+Ix.
 for mirror ratio 1:1 ratio iref is equal to Ix.

 the given values are,
 P= 1mw.
 vdd=1.8v.
 # Dc analysis :
 ![circit 1](https://github.com/user-attachments/assets/00468e5b-aada-45b8-808b-ab1ca0bd7ff9)
 
 we know that It=P/vdd.
 It = 1mw/1.8v = 0.55mA.
 Iref is half of the It value that is 0.275 mA.
 the given W/L values to get ratio 1:1 are 2.8um/180nm.
 we need to provide vin value such a way that the circuit should be in saturation . now the provided value is 0.854v.

 ## output for L = 180nm

![DC 1](https://github.com/user-attachments/assets/2804f44e-fb7c-4d80-823f-231d57bab637)

# for L =500nm




![l 2](https://github.com/user-attachments/assets/999a3f1d-9ae7-40d9-8126-0a7940a32c02)

# for L= 1um
![image](https://github.com/user-attachments/assets/2fc7019a-c414-48e0-91f0-c3b7c264232d)


# Transient analysis:
Transient Analysis is used to simulate the time-domain response of a circuit when a time-varying input (such as a sine wave or pulse) is applied. It helps in analyzing circuit behavior over time, including signal amplification, switching characteristics, and transient response.

**Transient Analysis Parameters:**
• Stop time: 10 ms  
• Step time: 1 µs  
• Time to start saving data: 0 s 


![Screenshot 2025-03-23 142520](https://github.com/user-attachments/assets/f3e6c49b-ad52-4c95-8ddc-dd652b266cef)



# AC analysis:

**Simulation Parameters:**
• Type of sweep: Decade  
• Number of points per decade: 10
• Start frequency: 0.1 Hz  
• Stop frequency: 1 THz  

**Input Signal Parameters:**
• Waveform Type: Sine Wave  
• Amplitude: 50 mV  
• DC Offset: 0.854 V  
• Frequency: 1 kHz 


![Screenshot 2025-03-23 143049](https://github.com/user-attachments/assets/c95c174b-2c9a-4caa-8c29-824175ff301e)


![Screenshot 2025-03-23 143140](https://github.com/user-attachments/assets/9e23f68d-3522-4b53-bf19-64cf16d4c7d3)

The obtained gain is 21.4 dB and the practical value is 20dB.


