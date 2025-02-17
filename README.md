# LICcourse
## Experiment-1

## Aim
Perform DC, transient, and AC analysis of a CS amplifier in LTSpice by setting up biasing, simulating the operating point for DC, using a pulse for transient, and applying an AC signal with small-signal analysis to extract parameters like Id,Vgs, voltage gain.

## Components required:
Mosfet(nmos4 ,pmos4 ), Resistor(1k ohm), voltage supply(1.8V,0.9V) and connecting wires.

## Theory
The Metal-Oxide-Semiconductor Field-Effect Transistor (MOSFET) is a crucial component in modern electronics, primarily due to its compact design, low power consumption, simple geometry, and compatibility with Very-Large-Scale Integration (VLSI) technology. MOSFETs are available in three primary configurations—common drain, common gate, and common source—with the common source configuration being the most widely used.

In the saturation region of operation, where the MOSFET functions as an amplifier, the conditions
 Vgs > Vth ,  Vgd < Vth, Vds > Vov (for an N-channel MOSFET) are satisfied. In the common source configuration, the output exhibits a 180-degree phase shift relative to the input. This configuration is known for its very high input impedance, which ideally approaches infinity, as the gate current is negligible. The drain current is a critical parameter for MOSFET operation and performance.

 The drain current
Id = 1/2 kn Vov^2 ; Vov=Vgs-Vth and kn=un Cox W/L
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
example:

## Circuit diagram

   ![Image](https://github.com/user-attachments/assets/32c4bb76-9c75-4343-b922-34e50bfb238f) 
    
   specifications Vin = 0.9v, Vdd=1.8v, Rd=1kohm, W=1um, L=180nm, Vth=0.366v


4. DC Analysis:
   - Set up the circuit as per the schematic diagram with proper connections to ensure it is valid for further analysis.
   - Apply a DC voltage of Vdd = 1.8V and Vgs = 0.9V.
   - Go to the Simulate menu, select Edit Simulation Command, choose DC Analysis, and click OK (.op).
   - Press Run to obtain the*DC operating point, output voltage (Vout), and drain current (Id).
    simulation
    ![Image](https://github.com/user-attachments/assets/975c5b9b-2687-4aaa-99b9-c6e1d1d9d725)

    the operating point is Vds=1.647v, Id=0.152mA,
    here Vgs = Vg-Vs = 0.9v, Vgs>Vth
     Vov=Vgs-Vth = 0.9- 0.366 = 0.534v,  Vds>Vov
     mosfet is in saturation region.


5. Transient Analysis:
   - Apply a sine wave input with Vgs = 0.9V, amplitude = 50mV, and frequency = 1kHz by going to the Advanced menu in the Voltage Source settings.
   - Go to the Simulate menu, select Edit Simulation Command, choose Transient Analysis, and set the Stop Time to **10ms (.tran 10m).
   - Press Run to visualize the circuit's response to a time-varying signal.
     simulation
     
     input waveform
     
     ![Image](https://github.com/user-attachments/assets/338c3594-c29a-42fd-80b6-22717bd1e6e2)
     
     output waveform
     
     ![Image](https://github.com/user-attachments/assets/ecb62034-5460-4af4-90b9-c88be4b8ffd9)
   
     

   6.AC Analysis:
   - Go to Spice Directive and provide the library file path for the simulator to access the data.
   - Go to the Simulate menu, select Edit Simulation Command, and choose AC Analysis. Set the sweep type to Decade, with 20 points per decade, and the frequency 
     range from 0.1Hz to 1THz.
   - Click OK (.ac dec 20 0.1 1T) and then Run to analyze the gain and frequency response of the circuit.
     simulation
     
     ![Image](https://github.com/user-attachments/assets/7ce515dd-1777-496e-b542-939973d7fda7)
     
     gm=0.569mS, Av=Vo/Vin = 2.13 v/v
     
     observations:
     when the width varies and the lenght is constant
     when W=1um,   Id = 0.152mA
     when W=0.5um, Id = 90.06uA
     when W=2um,   Id = 0.275mA
     when W=4um,   Id = 0.512mA
     Key Observation:The drain current increases with increasing width 𝑊W, as expected. This is because the MOSFET's current-carrying capability is directly 
                     proportional to the channel width 𝑊. A larger width provides a larger cross-sectional area for current flow, resulting in higher current.
## Result
1. DC Analysis:
   - Operating Point:
     

2. Transient Analysis:
   - Input Waveform: A sine wave with V_{GS} = 0.9V , amplitude =50 mV, and frequency = 1 kHz was applied.
   -Output Waveform:The output is an amplified and inverted version of the input signal, typical of a common-source amplifier.

3. AC Analysis:
   - Voltage Gain: A_v = 2.13 V/V
   -Transconductance:g_m = 0.569 mS
   - The frequency sweep from 0.1 Hz to 1 THz shows the frequency response, with a stable gain at lower frequencies and a roll-off at higher frequencies.

4. Variation of Drain Current with Width (W):
   - The drain current  increases with increasing MOSFET width
   - Larger values of  provide more current-carrying capacity, as seen in the trend
   - As  W increases, the current increases proportionally, demonstrating that **wider devices** can handle higher currents.


##  Inference

The simulation of the n-channel MOSFET shows that under the DC analysis, the device operates in the saturation region. This is confirmed by the conditions where the gate-to-source voltage  is greater than the threshold voltage , ensuring that the MOSFET is turned on, and the drain-to-source voltage  is sufficient to keep the device in saturation. In the transient analysis, the circuit amplifies the input signal, producing an output that is scaled and inverted, which is characteristic of a common-source amplifier. The AC analysis reveals that the circuit provides a voltage gain of 2.13 V/V and a transconductance of 0.569 mS, indicating the MOSFET's capacity for small-signal amplification. Overall, the results demonstrate how the circuit behaves in response to both DC and AC signals, emphasizing its suitability for amplification purposes in practical applications.
Variation of Drain Current with Width (W): When the width of the MOSFET is increased, the drain current also increases. This behavior is expected because a larger width increases the cross-sectional area available for current flow, allowing more current to pass through the MOSFET. The results highlight that the drain current is directly proportional to the width of the MOSFET, reinforcing the fact that larger devices with greater width provide higher current-carrying capability, which is a crucial factor in designing high-current or high-gain amplifiers.
     
## Question 1

Specifications: 180 nm technology, tsmc, VDD = 1.8 V, Power budget = 50 uW, do the DC analysis, Transient analysis, AC analysis,Extract the parameters- DC operating point, , gain.

   # circuit diagram
   
   ![Image](https://github.com/user-attachments/assets/391f92a2-eac8-4ff7-b00b-dd05635d026e)
   
   Vdd=1.8v, P= 50uW, Vin=0.9v, Vth=0.366v, Rd=1kohm
   P=Vdd.Id 
   Id=P/Vdd = 50u/1.8 = 27.77uA
   W=1.7um, L=1.8um
  
   # DC Analysis
   
   ![Image](https://github.com/user-attachments/assets/eef14870-5c6c-40d5-8c67-d7abee8c5187)
   
   here the operating point is Vds= 1.77226v , Id = 27.7uA 
    here Vgs = Vg-Vs = 0.9v, Vgs>Vth
    Vov=Vgs-Vth = 0.9- 0.366 = 0.534v,  Vds>Vov
    mosfet is in saturation region.
    
   # Transient analysis
   
   Input waveform

   ![Image](https://github.com/user-attachments/assets/fd520afc-66e6-42ee-980e-b71b05942d04)
   
   output waveform
   
   ![Image](https://github.com/user-attachments/assets/9406a59c-e375-447d-9e06-105338945a83)
   
   there is a 180 degree phaseshift between input and output.
   
   # AC Analysis
   
   ![Image](https://github.com/user-attachments/assets/2cd69681-e8c3-40f1-8aac-c6840a4fcb69)
   
   Av=1.99 v/v
   
   
## Question 2

Replace the resistor with a PMOS in Question 1 and do the DC analysis, Transient analysis, AC analysis,Extract the parameters- DC operating point,  gain, and verify the circuit.

   # circuit diagram
   
   ![Image](https://github.com/user-attachments/assets/91d66ec2-e201-435c-b9ef-93cbc68c213c)

   
   Vdd=1.8v, P= 50uW, Vin=0.9v, Vth=0.366v, Rd=1kohm, Vtp=-0.3906v
   P=Vdd.Id 
   Id=P/Vdd = 50u/1.8 = 27.77uA
   for NMOSFET W=1.7um, L=1.8um
   W/L=0.94
   Vds= 1.772v
   let the W/L ratio for the Pmosfet is same as the Nmosfet then 
   Idp=kpW(Vdd-Vb-|Vtp|)^2/2L
   kp=up.Cox 
   Cox = 8.307*10^-5 F/m^2
   kp=9.61mA/V^2
   Idp=kpW(Vdd-Vb-|Vtp|)^2/2L
   by substituting and the calculations 
   -1.98029 = Vb^2 - 2.818Vb
   by solving this equation
   Vb = 1.33v or 1.47v
   hence the value of Vb = 1.33v
   
   # DC Analysis
   ![Image](https://github.com/user-attachments/assets/5f8b9804-5437-4cca-b35c-552a660f2e39)

   
   here the operating point is Vds= 1.772v , Id = 27.7uA 
    for NMOSFET, Vgs = Vg-Vs = 0.9v, Vgs<Vth
    Vov=Vgs-Vth = 0.9- 0.366 = 0.534v,  Vds>Vov
    nmosfet is in saturation region.
    for PMOSFET  Vgs = Vg-Vs = O.33-1.8=-1.47, Vgs>Vth
    |Vov||= |Vgs|-Vtp|| = 1.47- 0.39 = 1.08,  |Vds| > |Vov|
    pmosfet is in saturation region.
   
   # Transient analysis
   input waveform
   
   ![Image](https://github.com/user-attachments/assets/f74f3e20-542f-4cdf-baf8-ebfc1f543f7e)
   
   output waveform
   
   ![Image](https://github.com/user-attachments/assets/2d782cd2-404b-43bf-bd8f-752cd933e92e)
   
   there is a 180 degree phaseshift between input and output.
   
   # AC Analysis
   
   ![Image](https://github.com/user-attachments/assets/045ffa52-1804-4731-9d67-371aa24a0795)
   
   Av=Vo/Vin = 1.99 v/v

   
 # Inference
In both Question 1 and Question 2, the MOSFET-based amplifier circuit was analyzed through DC, transient, and AC analyses. In Question 1, the circuit uses a resistor as the load, while in Question 2, the resistor is replaced by a PMOSFET. This replacement is done to improve the overall performance of the amplifier. The PMOS transistor acts as an active load, which enhances the voltage gain and linearity of the circuit, offering a better dynamic load than a static resistor. The PMOS load ensures that the output remains more stable and less affected by supply voltage fluctuations, maintaining a higher degree of amplification efficiency. Additionally, using a PMOS transistor reduces power consumption compared to a resistor because the transistor can more effectively control the current flow, avoiding the heat dissipation seen with resistors. The DC analysis confirms the operating point of both circuits, showing that both the NMOS and PMOS configurations are in the saturation region, with a drain current of 27.7 µA and a drain-source voltage of 1.772V. In transient analysis, both circuits exhibit a 180-degree phase shift between the input and output signals, indicating their behavior as common-source amplifiers, where the input signal is inverted. The AC analysis shows a voltage gain of 1.99 V/V for both configurations, demonstrating the circuit's effectiveness in signal amplification. Ultimately, the substitution of the PMOSFET transistor for the resistor significantly improves the performance by providing a more efficient and linear load, enhancing voltage gain, output swing, and power efficiency. This modification enables the amplifier to perform better in amplification applications, confirming that both NMOSFET and PMOSFET can effectively operate in such circuits with similar results.
    
   
   






