# LICcourse
##Experiment-1

## Aim
Perform DC, transient, and AC analysis of a CS amplifier in LTSpice by setting up biasing, simulating the operating point for DC, using a pulse for transient, and applying an AC signal with small-signal analysis to extract parameters like Id,Vgs, voltage gain.

##Components required:
Mosfet(nmos4 ,pmos4 ), Resistor(1k ohm), voltage supply(1.8V,0.9V) and connecting wires.

## Theory
The Metal-Oxide-Semiconductor Field-Effect Transistor (MOSFET) is a crucial component in modern electronics, primarily due to its compact design, low power consumption, simple geometry, and compatibility with Very-Large-Scale Integration (VLSI) technology. MOSFETs are available in three primary configurations—common drain, common gate, and common source—with the common source configuration being the most widely used.

In the saturation region of operation, where the MOSFET functions as an amplifier, the conditions
 Vgs > Vth ,  Vgd < Vth, Vds > Vov (for an N-channel MOSFET) are satisfied. In the common source configuration, the output exhibits a 180-degree phase shift relative to the input. This configuration is known for its very high input impedance, which ideally approaches infinity, as the gate current is negligible. The drain current is a critical parameter for MOSFET operation and performance.

 The drain current
Id = 1/2 kn Vov2 ; Vov=Vgs-Vth and kn=un Cox W/L
Output is taken from the drain end rather than simply across the resistor to maintain the common ground referance.

## DC Analysis
DC analysis is essential for ensuring that the MOSFET operates in the saturation region and for determining the transistor's DC operating point. This is crucial for preventing signal distortion during amplification. The analysis aids in selecting appropriate biasing resistors and ensures the transistor maintains a stable operating point, even in the presence of fluctuations in other circuit parameters. By establishing a proper bias point, DC analysis guarantees optimal performance and reliability of the MOSFET in the amplifier circuit. 

## Transient Analysis
Transient analysis is performed to examine the circuit's response to time-varying signals. It is crucial for identifying signal distortions, DC shifts, and phase discrepancies between the input and output. This analysis is instrumental in detecting issues such as phase distortion, which can significantly impact signal integrity. Additionally, transient analysis is essential in high-speed applications, such as communication systems, where accurate signal behavior and timely responses are critical for optimal performance.

## AC Analysis
AC analysis, or small-signal analysis, is performed to evaluate the gain of the amplifier circuit and assess its frequency response. This analysis helps determine the amplifier's behavior under small input variations around the operating point. The voltage gain ( Av ) of the amplifier is given by Av = -gm.RD , where gm  is the transconductance and RDis the drain resistor. AC analysis is essential for understanding how the circuit amplifies signals at different frequencies, ensuring efficient performance across the desired frequency range.

## Procedure
1. Create a Folder:
   - Create a new folder on your system. Save the tsmc018.lib file in this folder for easy access.
2. Save Schematic File:
   - Open a new schematic file in LTSpice and save it in the folder you created earlier. To include the tsmc model, insert the library file by typing .lib tsmc018.lib in the schematic.
3. Configuration:
   - Select the MOSFET in the schematic and attach the tsmc model. Name the MOSFET CMOSN . Set the length to 1.8µm and width to 1.7µm. then select the resistor of 1kohm and voltage source of 1.8v and 0.9v. set 
    up the circuit as in the circuit diagram.
## Circuit diagram
![Image](https://github.com/user-attachments/assets/32c4bb76-9c75-4343-b922-34e50bfb238f)


4. DC Analysis:
   - Set up the circuit as per the schematic diagram with proper connections to ensure it is valid for further analysis.
   - Apply a DC voltage of Vdd = 1.8V and Vgs = 0.9V.
   - Go to the Simulate menu, select Edit Simulation Command, choose DC Analysis, and click OK (.op).
   - Press Run to obtain the*DC operating point, output voltage (Vout), and drain current (Id).
    simulation
![Image](https://github.com/user-attachments/assets/975c5b9b-2687-4aaa-99b9-c6e1d1d9d725)


5. Transient Analysis:
   - Apply a sine wave input with Vgs = 0.9V, amplitude = 50mV, and frequency = 1kHz by going to the Advanced menu in the Voltage Source settings.
   - Go to the Simulate menu, select Edit Simulation Command, choose Transient Analysis, and set the Stop Time to **10ms (.tran 10m).
   - Press Run to visualize the circuit's response to a time-varying signal.
     simulation
     ![Image](https://github.com/user-attachments/assets/338c3594-c29a-42fd-80b6-22717bd1e6e2)

![Image](https://github.com/user-attachments/assets/ecb62034-5460-4af4-90b9-c88be4b8ffd9)

   6.AC Analysis:
   - Go to Spice Directive and provide the library file path for the simulator to access the data.
   - Go to the Simulate menu, select Edit Simulation Command, and choose AC Analysis. Set the sweep type to Decade, with 20 points per decade, and the frequency range from **0.1Hz to 1THz**.
   - Click OK (.ac dec 20 0.1 1T) and then Run to analyze the gain and frequency response of the circuit.
     simulation
     ![Image](https://github.com/user-attachments/assets/7ce515dd-1777-496e-b542-939973d7fda7)
     

By following these steps, you will perform the DC, transient, and AC analysis of the MOSFET circuit using LTSpice, allowing you to observe the operating point, time response, and frequency characteristics.
