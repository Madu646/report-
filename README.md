# Experiment-1
# Aim:
To do the DC analysis,Transient and AC analysis of a CS amplifier circuit and 
extract the various parameters associated using LT Spice.
# Components required: 
Resistor(22k),voltage supply(1.8V,0.9V), connecting wires and N Mosfet(nmos4,pmos4 )
# Theory:
MOSFET is the most important component in the electronic devices 
mosfet act as amplifier in saturation region when vgs>vth and vgd<vth or vds>=vov
# CONFIGURATIONS:
1) common source configuration - there is 180' phase  diffrence between input and output
2) common drain configuration - there is no phase diffrence between input and output
3) common gate configuration - there is no phase diffrence between input and output

There is very high input impedence
The drain current

**Id= 1/2*kn*(Vov)^2**; **Vov=Vgs-Vth & kn=W/L*un*Cox** for lambda = 0.
Output is taken from the drain end rather than simply across the resistor to maintain the common ground referance.

The different analysis i.e DC Analysis is done to ensure the mosfet operates in saturation so that the the mosfet works as an amplifier.

Transient Analysis is done to anlalise the response of the amplifier to the time varying input sine wave and the corresponding output.

AC Analysis is done to evaluate the gain of the amplifier which is **-gm*Rd**;gm is transconductance of the amplifier.
# Procedure:
1.Create a new folder and name it as project file.Save the LT spice file in this folder.

2.Name the mosfet as CMOSN and the length as 180nm and width as 3um initially.

3.For the pmos name it as CMOSP and set the length as 180nm and width as 3um respectively

4.**DC Analysis:** Set up the circuit as per the circuit diagram with proper connections ensuring valid circuit for further analysis.
Apply the DC voltage of Vdd=1.8V and Vgs = 0.9 V . Go to simulate option in the tab and edit simulation command, click on DC analysis and press ok.(.op)
Click on Run in the tab menu to get the DC operating point ,Vout and Id.

5.**Transient Analysis:** Apply a sine wave input of Vgs=0.9V with an amplitude of 50mV and frequency of 1kHz by going to advanced menu in the voltage setting option.go to simulate option in tab ,edit simulation command 
, click on transient analysis and give the stop time as 3m and click ok.(.tran 3m) Now Run to visualise the response of the circuit to a time varying signal.

6.**AC Analysis:** Go to spice directive and give the library file path for the simulator to access the data through the path . Go to simulate option in the tab , edit simulation command , click on AC analysis 
and mention the time of sweep as decade , no of points as 20 and frequency as .1Hz to 1THzand click on ok.Now Run to analyze the gain and frequency response of the circuit.(.ac dec 20 .1 1T)
# CIRCUIT 1 :
![Image](https://github.com/user-attachments/assets/b465a764-eadb-480b-b600-e1f4ce22460c)
# Calculation :
Power = 100uW

Loop Equation: Vdd=Vds+Id*Rd

P=I*V (Id=55.55 uA , Vdd=1.8V)

clearly Vds=Vout; Vds>=Vgs-Vth

Rd (upon calculation) =22.6Kohm 

Widhth=0.3um(Vary width to get the current)

Vds=0.543

gain=-20dB(from AC analysis)

Q point is (0.543,55.55uA)
# Tabular Column :

|Width |  Current(Id) |  Vout |

|1um   |  74.2uA      | 0.122 |

|0.8um |  72.7uA      | 0.155 |

|0.7um |  71.65uA     | 0.18  |

|0.5um |  67.2uA      | 0.27  |

|0.3um |  55.55uA     | 0.543 | 

# Results:
1.**DC Analysis:**
![Image](https://github.com/user-attachments/assets/cc89c473-d04e-43b0-876a-cc85adb4e72b)





Id=55.55uA

Vout=0.543V

Width=0.3um

DC Operating point : (0.543,55uA) is obtained for 0.3um Width and 180nm Length.

2.**Transient Analysis:**
![Image](https://github.com/user-attachments/assets/2d6359aa-d9c0-4f9a-a694-33de7b46a88e)

Vout=0.543V
There is 180 degree phase shift between input and output or the DC level shift.
3.**AC Analysis:**

![Image](https://github.com/user-attachments/assets/0c964316-3b66-4b0c-ae63-22b0d93d580c)

Gain=-20dB
# inference :
1) The current equation id tells  that current is directly proportional to the width and inversly proportional to the length.
2) The mosfet must operate in the saturation region to get desired negative gain.
3)  A stable Q-point is achieved in the saturation region, which is essential for linear amplification
4)  There is 180' phase diffrence between output and input
5)  MOSFET amplifier acheives maximum gain in mid band frequency. 








