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
![image](https://github.com/user-attachments/assets/5a89b1e5-8888-429a-9439-d255a512ab92)



# Transient analysis:
Transient Analysis is used to simulate the time-domain response of a circuit when a time-varying input (such as a sine wave or pulse) is applied. It helps in analyzing circuit behavior over time, including signal amplification, switching characteristics, and transient response.

**Transient Analysis Parameters:**
• Stop time: 10 ms  
• Step time: 2ms 
• Time to start saving data: 0 s 


![Screenshot 2025-03-23 142520](https://github.com/user-attachments/assets/f3e6c49b-ad52-4c95-8ddc-dd652b266cef)

the obtained gain is equal to vout/vin

vout/vin = 10.15v/v

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
# 3dB:
The obtained 3dB bandwidth is 316.22khz


# For the ratio 1:2
### Calculations:
* Power <= 1mW
* Vdd = 1.8V
* I<sub>total</sub> = power/Vdd = 1mW/1.8 = 55.5mA
* I<sub>D</sub>= I<sub>total</sub>/3 = 0.185mA.
* 1:2 ratio = 0.185mA : 0.37mA.
  # DC analysis:
  1.Case 1: 180nm
# circuit diagram:
![image](https://github.com/user-attachments/assets/6a2c61fb-ff40-4477-bab7-c28e810dff37)

# output:
![image](https://github.com/user-attachments/assets/19442ae1-dbe3-4fea-b24b-05eb9f14d5c6)


Vout= 1.20094V
Vx= 1.20934V
Itotal = 0.185mA\
PMOSFET 1 = length is 180nm, width is 70um 

PMOSFET 2 = width is 140nm

NMOSFET = length is 180nm, width is 135.867um
# case 2:
L= 500nm
# output:
![image](https://github.com/user-attachments/assets/20ff9a2e-6b42-4161-9223-3bd102b50df7)
# case 3:
L =1um
# output:
![image](https://github.com/user-attachments/assets/30cb1a5a-2f3c-400a-8705-02d46b21f8ea)
# transient analysis:
Replace DC input with an AC signal.
Use SINE(dc_offset, Amplitude, Frequency).
Go to "Simulate" > "Edit Simulation Cmd" > "Transient".
Set Stop Time: 10ms.
Run the simulation.
Our dc_offset = 0.854V and assume amplitude as 50mV and frequency as 1Khz.
![image](https://github.com/user-attachments/assets/4cc70489-f8dd-40d0-9507-82765e440c0d)
The obtained gain is 11.68v/v
# AC analysis:
![image](https://github.com/user-attachments/assets/83039d9f-a4ef-4b74-b2dd-2f3f37d59dea)

# 3dB bandwidth:
![image](https://github.com/user-attachments/assets/2ac97934-2c2f-465a-9ff4-43923eea5f61)

# inference:
1)Transient analysis of the amplifier with the 1:1 current mirror configuration (L=180nm) yielded a voltage gain (Av) of 10.15 V/V , which is slightly above the design Av > 10.

2)The experiment confirms that channel length modulation significantly impacts current mirror accuracy
3)the current ix slightly increases whwn we did 1:2 ratio.

# PART -B:
# circuit diagram with aim:
![image](https://github.com/user-attachments/assets/d8e8f8ea-a001-4c30-8789-9faacef4670f)

# circuit:
![image](https://github.com/user-attachments/assets/67de3451-8b0c-4300-b441-6a1444a78330)

# dc analysis:


![Screenshot 2025-03-24 113334](https://github.com/user-attachments/assets/d930b666-b3ed-43b3-90ff-97ec5059c650)
as per the parameters of the differential amplifier Vdd = 2.5V, Id(M1 and M2)=0.608mA, Vout = 1.38V and as per the circuit question current mirror ratio of M3 amd M4 1:2.

 we need to give Iref =0.608mA keeping L=180nm constant for all the mosfet for perfect current mirroring, by trial and error width was found to be W(4) = 3.5um, W(3) = 3.5um. W3 is double the W4 because we need to double increase the Id(M3).

# Transient analysis:
![image](https://github.com/user-attachments/assets/846f27fd-085c-4d0f-b8b2-995e48d34220)

# AC analysis:

![image](https://github.com/user-attachments/assets/df0b1542-3652-46e2-bff4-fa98989fa9e9)
# conclusion :
Current mirrors play a crucial role in biasing circuits, especially in differential amplifiers, ensuring stable operation with minimal variation. By implementing NMOS current mirrors as bias voltage generators, differential amplifiers achieve better gain, stability, and power efficiency, making them a key component in modern analog IC design.


