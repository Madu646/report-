### **"Differential Amplifier"**

Differentiator amplifier, also known as a differentiating amplifier or a differentiator circuit, is an operational amplifier in which output voltage is directly proportional to the input's time derivative. In simpler words, the output voltage can be modified based on the time derivative or the RC time constant.
What does a differential amplifier do?
The purpose of the differential amplifier is to increase the amplitude of the heart signal to a level where it can be converted into a digital form. The gain of the circuit can be adjusted by appropriate selection of external resistors connected between the output and input terminals.
### **question:Vdd=2.5v , p<=3mw , Vicm=1.3v, Vocm=1.25v , Vp=0.5v , vocm=1.4v**
**Circuit 1** <br>
![Image](https://github.com/user-attachments/assets/4a8c18fd-31d4-42e2-84f7-ccaa40dd426d)


### Step 1:Dc analysis design Rd and Rss
![dc calc](https://github.com/user-attachments/assets/9effe2da-0b1a-43fd-aa7e-5bf8af3cdf2d)



from the calculation we have finded Iss value as 1mA <br>
Id1 and Id2 as 0.5mA <br>
Rd as 1.833kohm <br>
Rss as 416.66ohm <br>
Vgs=vg - vp = 1.3v - 0.5v = 0.8v <br>
Vov = vgs - vth = 0.8v - 0.366v = 0.434v <br>

To set the operating point go to Configure Analysis and select Dc operating Point <br>

to set correct operating point vary width and length values 
width =8.05u <br>
length = 180n <br>


![Screenshot 2025-03-04 183108](https://github.com/user-attachments/assets/29bcd7c2-01f8-4ccd-8868-6e676a54e5b3)

### **Analysis**

**Increase Vicm from 1.3v to 1.4v and observe Vocm and Vp** <br>
| **Common-Mode Input Voltage (V_ICM)** | **Output Voltage (V_out)** | **Voltage at Point P (V_P)** |
|--------------------------------------|--------------------------|--------------------------|
| **1.3V**                            | **1.38484V**             | **0.5V**                |
| **1.4V**                            | **1.23925V**                 | **0.572037V**               |




![Screenshot 2025-03-04 183146](https://github.com/user-attachments/assets/9ac2d4c0-65d6-4c50-9f07-6bba79589cb3)
### Effect of VICM on Vout and vp

As the common-mode input voltage \( VICM \) increases, the source voltage \( VP \) also increases, causing a shift in the operating point. This leads to a higher drain current, resulting in a greater voltage drop across \( RD \), which reduces \( Vout \).

### **Calculate maximum input ,output Swing  and gain**

change amplitude value from 50m to 600m




![Screenshot 2025-03-04 184021](https://github.com/user-attachments/assets/0164cb4d-2498-4a61-9d69-3bc4b7263f45)



![Screenshot 2025-03-04 104945](https://github.com/user-attachments/assets/e10f6351-9e54-4a54-9a92-3483ef9dcb76)
### **TRANSIENT ANALYSIS**
go to configure Analysis and select transient analysis then <br>
stop time as 5m <br>
time to start saving data as 0 <br>

• Waveform Type: Sine Wave
• Amplitude: 20 mV
• DC Offset: 1.3V
• Frequency: 1 kHz

And in V2 phi(deg) as 180


![Screenshot 2025-03-04 190934](https://github.com/user-attachments/assets/d61525d3-b43a-4dd1-8ada-21d0767d6c94)
### **AC Analysis**

go to configure analysis and select AC Analysis
• Type of sweep: Decade
• Number of points per decade: 5
• Start frequency: 0.1 Hz
• Stop frequency: 1 THz

Set <br>
AC Amplitude as 1 and AC Phase as 0 in V1 <br>
AC Amplitude as 1 and AC Phase as 180 in V2 <br>


![Screenshot 2025-03-04 191749](https://github.com/user-attachments/assets/84496068-358c-4a9d-9a47-9233deccde8e)


![Screenshot 2025-03-04 192520](https://github.com/user-attachments/assets/e98c280e-085f-4943-af51-a74986cc7228)

### CIRCUIT 2:
Replacing resistor with current source

![Screenshot 2025-03-04 193927](https://github.com/user-attachments/assets/58d25de9-2acd-45fb-bedf-93c3b865662a)
# DC ANALYSIS:

![Screenshot 2025-03-04 193540](https://github.com/user-attachments/assets/e5736bde-72ff-4d48-869f-b9d4794621c1)
### **Analysis**

**Increase Vicm from 1.3v to 1.4v and observe Vocm and Vp** <br>

| **Common-Mode Input Voltage (V_ICM)** | **Output Voltage (V_out)** | **Voltage at Point P (V_P)** |
|--------------------------------------|--------------------------|--------------------------|
| **1.3V**                            | **1.587**             | **0.537**                |
| **1.4V**                            | **1.587V**                 | **0.634**               |


![Screenshot 2025-03-04 193803](https://github.com/user-attachments/assets/a6a491b0-53ed-4f60-ac84-862a4e9531ee)
# transient analysis:


![Screenshot 2025-03-04 195407](https://github.com/user-attachments/assets/48474381-dae1-4dbd-af4a-828f2c4dbea9)

By changing amplitude from 20mv to 500 mv


![Screenshot 2025-03-04 195034](https://github.com/user-attachments/assets/32784df2-340d-4ff7-8c9e-b73e019e3efb)

### AC ANALYSIS :

![Screenshot 2025-03-04 195813](https://github.com/user-attachments/assets/9459856e-2c86-4cbd-b613-21fa5706749d)

### CIRCUIT 3:
Replacing current Source with MOSFET 


![Screenshot 2025-03-04 200424](https://github.com/user-attachments/assets/29db27ff-2882-4c49-bce8-ee48b11dc4e2)
How to find Vb?
Vb = vth + Vp <br>
Vb = 0.366v + 0.5v <br>
Vb = 0.866v <br>
To set the operating point vary 3rd MOSFET width and keep length as same before 
For approx operating Point i got width as 12.6u

# dc analysis:


![Screenshot 2025-03-04 201336](https://github.com/user-attachments/assets/aa465d5c-54cc-4657-84ed-256c35610e47)
**Increase Vicm from 1.3v to 1.4v and observe Vocm and Vp** <br>

| **Common-Mode Input Voltage (V_ICM)** | **Output Voltage (V_out)** | **Voltage at Point P (V_P)** |
|--------------------------------------|--------------------------|--------------------------|
| **1.3V**                            | **1.394v**             | **0.497v**                |
| **1.4V**                            | **1.368V**                 | **0.587v**               |



![Screenshot 2025-03-04 201411](https://github.com/user-attachments/assets/a39e7127-5adb-429a-a985-9055d03b5696)
# transient analysis:




![trans 1](https://github.com/user-attachments/assets/1258abba-908d-48dd-bfaa-5a02670745d1)

BY changing amplitude from 20mv to 500mv
input and output swing




![amp 1](https://github.com/user-attachments/assets/2dc7b33f-2bec-4d5d-965d-d470cdeb7393)

# AC ANALYSIS:



![ac 1](https://github.com/user-attachments/assets/3f790afc-ef6f-4237-b407-fd6b32626083)


# Inference:  

This experiment explored differential amplifier configurations: resistor-based, current source-based, and NMOS-based, each affecting gain, bandwidth, and stability differently.  

- Resistor: High bandwidth, low gain, low CMRR.  
- Current source: High gain, high CMRR, slightly lower bandwidth.  
- NMOS (CMOSN): Highest gain.  

 Best Configuration Based on Need:  
1. High bandwidth → Resistor  
2. Maximum gain→ NMOS (CMOSN)  
3. Better CMRR→ Current source or NMOS (CMOSN)

## result:
1. **Circuit-1:**  
   - The transient response confirms that the circuit behaves correctly as a differential pair.  
   - The AC analysis indicates a decent gain and good common-mode noise rejection.  
   - The DC analysis shows that the MOSFETs work in saturation and have equal drain currents when the input voltages match.  

2. **Circuit-2:**  
   - The transient response is more balanced, leading to better symmetry in the signals.  
   - The AC analysis shows that this circuit has higher gain and a wider frequency range than Circuit-1.  
   - Using a current source instead of a resistor makes the biasing more stable, as seen in the DC analysis.  

3. **Circuit-3:**  
   - The transient response ensures signal accuracy with improved performance.  
   - The AC analysis shows even higher gain and a broader frequency range.  
   - The DC sweep analysis confirms that the output changes as expected.  
   - The DC analysis confirms that the MOSFET-based current source effectively controls the tail current.


### CIRCUIT 4:


![Screenshot 2025-03-04 223152](https://github.com/user-attachments/assets/6646efcb-08b5-4458-892c-9e4e8676b95d)

## DC ANALYSIS:



![Screenshot 2025-03-04 224318](https://github.com/user-attachments/assets/5bd7277d-3990-48a5-8ac8-94ac43c8be45)



