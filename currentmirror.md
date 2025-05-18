
## Lic-lab
## Experiment-3
<p>Differential amplifier analysis</p><br>
<p>This experiment shows the ac,dc and transient analysis of Differential amplifier </p><br>
<p>Question : Design Differential amplifier for the following specifications vdd=2.5v ,vicm=1.3v ,vocm=1.4v, vp=0.5v. Perform Dc analysis, transient analysis, frequency response and extract the required parameters.</p><br>

![IMG_20250306_111047](https://github.com/user-attachments/assets/b9440e5f-9ce8-491f-911c-5ba7b42cfbde)

## Abstract
<p> We need to design a differential amplifier that meets specific voltage and input signal criteria. The design process involves performing four essential analyses: DC Analysis to establish the amplifier's operating point, Transient Analysis to observe its response to varying signals, Frequency Response Analysis to evaluate its performance across a range of frequencies, and Parameter Extraction to collect critical information like gain and bandwidth. Additionally, we need to determine the input and output swing of the amplifier. The objective is to ensure the amplifier operates optimally within the defined specifications.
</p>

## Theory

<p>A differential amplifier is an electronic device specifically designed to amplify the voltage difference between two input signals, providing high accuracy and noise immunity. It has two inputs: a non-inverting input and an inverting input. The amplifier boosts the voltage difference between these two inputs while rejecting any voltage that is common to both, referred to as the common-mode voltage. <br>
 This ability to reject common-mode signals is quantified by the common-mode rejection ratio (CMRR), which measures the amplifier's effectiveness in ignoring noise or interference that affects both inputs equally. Differential amplifiers are widely used in applications such as signal processing, instrumentation, and communication systems, where it is essential to amplify weak signals in the presence of noise or other unwanted interference. By focusing only on the difference between the two inputs, differential amplifiers can effectively filter out external disturbances, making them invaluable in environments with high levels of electromagnetic interference. <br>
 
 For example, in medical instrumentation like electrocardiogram (ECG) machines, differential amplifiers help isolate the small electrical signals from the heart while rejecting noise from other sources. Similarly, in communication systems, they ensure that the desired signal is amplified while minimizing the effect of common-mode noise, ensuring clear and reliable signal transmission.
</p>

![17412325438756253492796588430102](https://github.com/user-attachments/assets/a7f5255d-0e60-4c25-9ab6-ad3db0235aa2)

<p>A differential amplifier amplifies the difference between two input voltages—V₁ (non-inverting) and V₂ (inverting)—and provides an output that is proportional to this difference. The key feature is its common-mode rejection ratio (CMRR), which quantifies how well the amplifier rejects signals that are common to both inputs. A high CMRR means the amplifier is effective at rejecting noise or interference that affects both inputs equally.</p>

# circuit 1
![Screenshot 2025-03-06 210045](https://github.com/user-attachments/assets/ed1a69bd-722b-4447-a0e2-663c1433e253)


<p>This circuit consists of two nmos transistors ,3 resistors 2 voltage sources and vdd</p>
<p>mosfets of length 180nm</p>
<p>mosfets of width 1um</p>
<p>rd of 1.8k ohm</p>
<p>rss of 416.66 ohm</p>
<p>vdd of 2.5v</p>
<p>vicm of each 1.3v</p>

![IMG_20250306_113636](https://github.com/user-attachments/assets/af6a8f49-7887-4ae5-86e3-9c5ef91b6550)
<p> We can observe that the circuit is in saturation region</p>



#  Dc analysis
<p>The DC analysis of a differential amplifier involves determining the biasing conditions of the circuit when no input signal is applied (i.e., with a constant DC voltage). This analysis helps set the operating point of the transistors, ensuring they work in their active region. Key parameters like the quiescent currents, voltages across components, and the overall stability of the circuit are determined. DC analysis is essential for setting the proper biasing to ensure the amplifier functions correctly when signals are later applied.</p>

![Screenshot 2025-03-06 210137](https://github.com/user-attachments/assets/d37266d9-fb55-4509-8a5c-2b52124f7953)


![Screenshot 2025-03-06 210103](https://github.com/user-attachments/assets/4df2c097-f7f3-464d-aa31-0ea4c6387eaf)



<br>
<p>This  differential amplifier circuit has two resistors each of 1.8k,two voltage source of 1.3v,vdd=2.5v</p>
<p>Mosfet length= 180nm</p>
<p>width=7.918um</p>
<p>Q point is(1.4v,0.6mA)</p>
<br>

![Screenshot 2025-03-06 210206](https://github.com/user-attachments/assets/fe414bee-0801-4095-a4b7-43f1ccb94c16)

<p>The above image shows the other parameters of the mosfet like v<sub>gs</sub>,v<sub>t</sub> ,g<sub>m</sub> v<sub>ds</sub> and others</p>
<br>

# Transient analysis

<p>Transient analysis of a differential amplifier studies how the circuit responds to changes in the input signal over time. It simulates the amplifier’s behavior when the input voltage suddenly changes, such as when a pulse or step input is applied. This analysis helps determine how quickly the amplifier can respond, including how long it takes to reach a stable output, known as rise time, fall time, and settling time. It ensures the amplifier can accurately amplify signals without distortion or delays when dealing with real-time, rapidly changing inputs.</p>
<p>Transient analysis of Input</p>  
<br>

![Screenshot 2025-03-06 210358](https://github.com/user-attachments/assets/a8a39f5e-5de5-4f91-b641-401e063ee6ef)

<p>Transient analysis of output</p>  
<br>

![Screenshot 2025-03-06 210341](https://github.com/user-attachments/assets/88039cb6-b2a4-42cc-ba47-1309845bd121)

<p>Transient analysis of both input and output</p>
<br>

![Screenshot 2025-03-06 210415](https://github.com/user-attachments/assets/1d00df0a-6a68-4632-a15e-83c2bf0d0395)


<br>
<p>From the above figure we can clearly observe ,the 180 degree phase shift between input and output</p>
<p>A<sub>v</sub>=V<sub>out</sub>/V<sub>in</sub></p>
<p>From graph we have v p-p voltages as</p>
<p>V<sub>in</sub>=1.34929-1.25104=0.09825</p>
<p>V<sub>out</sub>=1.4805-1.3393=0.1412</p>
<p>A<sub>v</sub>=V<sub>out</sub>/V<sub>in</sub>=0.1412/0.09825=1.43715 V/V</p>
<br>

# Ac analysis

<p> AC analysis of a differential amplifier looks at how the amplifier responds to changing input signals, like alternating current (AC) signals. It helps determine how much the amplifier amplifies the input signal (gain) and how well it performs across different frequencies. This analysis shows the frequency response, such as the bandwidth and cutoff points, which indicates how effectively the amplifier handles high or low-frequency signals. Essentially, AC analysis helps ensure the amplifier works well with real-world, time-varying signals.</p>
<p>Ac analysis</p>
<br>

![Screenshot 2025-03-06 233119](https://github.com/user-attachments/assets/4c56f174-2841-4e19-a8f5-3be83d6efa6e)
<p>maximum gain</p>

![Screenshot 2025-03-06 233146](https://github.com/user-attachments/assets/014987a7-4eda-429a-acd6-a3504e13b948)



<br><p>From the above figure we can note the maximum gain in db </p>
<p>A<sub>v</sub> in db=3.15db</p>

<br><Also we can calculate the gain by formula A <sub>V</sub>=20log(vout/vin)=20log(1.43715)=3.15 v/v


<br><p>Gain remains constant as their is no change in R<sub>d</sub>.

# Input swing
<p>The input swing of a differential amplifier refers to the range of input voltages over which the amplifier can operate correctly without distortion. It represents the minimum and maximum input voltages that can be applied to the amplifier's inputs while still allowing it to produce an accurate output. If the input signal goes beyond this range, the amplifier may enter saturation or cutoff, causing the output to be distorted or clipped. The input swing is important for ensuring the amplifier can handle varying input signals without losing performance.</p>
<p>The DC offset here is done by taking the average of V<sub>in min</sub> and V<sub>in max</sub></p>
<p>V<sub>in cm_ min</sub>=V<sub>t N</sub> + V<sub>p</sub> = 0.36+0.44 = 0.8 </p>
<p>V<sub>in cm_max</sub>=V<sub>dd</sub>-R<sub>d</sub>I<sub>ss</sub>/2 +V<sub>t</sub>=2.5+(1.2m*1.82k)/2+0.36 = 1.768</p><br>
<p>  V<sub>in cm</sub>=( V<sub>in cm_ min</sub>+V<sub>in cm_ max)/2= 1.264</sub></p>
<br>
<p>V<sub>o cm_ min</sub>=V<sub>ov1</sub>+V<sub>ov2=0.88</sub></p>
<p>V<sub>o cm_ max</sub>=VDD-I<sub>d</sub>*R<sub>d=0</sub>=2.5-(0.6m*1.82k)=1.408</p>
<p>  V<sub>o cm</sub>=( V<sub>o cm_ min</sub>+V<sub>o cm_ max)/2= 1.144</sub></p>
<br>
<br>

<p>Input and output swing of mos1</p>

![Screenshot 2025-03-06 211118](https://github.com/user-attachments/assets/bc0fd866-a672-497c-b19a-af65e6e1ff00)
<br>
<br>
<p>Input and output swing of both mos</p>

![Screenshot 2025-03-06 211225](https://github.com/user-attachments/assets/f79ba66b-e04a-49de-bbfa-8e6439c228cb)


# circuit 2
<p>In this circuit we have replaced the resistor with a current source with I<sub>ss</sub>=1.2mA</p>

![Screenshot 2025-03-06 211446](https://github.com/user-attachments/assets/6f6d8db5-a8c0-4ff2-862f-411778dfc7cf)


<p>This circuit consists of two nmos transistors ,2 resistors 2 voltage sources ,a current source and vdd</p>
<p>mosfets of length 180nm</p>
<p>mosfets of width 1um</p>
<p>rd of 1.83k ohm</p>
<p>Iss of 1.2mA</p>
<p>vdd of 2.5v</p>
<p>vicm of each 1.3v</p>

#  Dc analysis

![Screenshot 2025-03-06 211510](https://github.com/user-attachments/assets/53c4cb26-8c7c-46c7-835d-8d14ddd8841a)

![Screenshot 2025-03-06 211624](https://github.com/user-attachments/assets/c83c7345-3bff-4cfc-a7bb-f63d1fc1858a)
<br>
<br><p>This  differential amplifier circuit has two resistors each of 1.83k,two voltage source of 1.3v,vdd=2.5v</p>
<p>Mosfet length= 180nm</p>
<p>width=7.918um</p>
<p>Q point is(1.4v,0.6mA)</p>
<br>

![Screenshot 2025-03-06 211549](https://github.com/user-attachments/assets/07e96428-e6e0-4a21-ba22-7464656bf6e4)
<br>



 #  Transient analysis
 
 <p>Transient analysis of Input</p>  
 
 ![Screenshot 2025-03-06 211801](https://github.com/user-attachments/assets/0f30f996-9059-425a-9094-c8c3951bb267)

 <p>Transient analysis of output</p>  
 
 ![Screenshot 2025-03-06 211744](https://github.com/user-attachments/assets/8fd9f8ab-bf2e-4c1c-8dfe-b95a5e0d8a54)
 <br>

 ![Screenshot 2025-03-06 211819](https://github.com/user-attachments/assets/a1f0fa26-d33d-4603-9078-6881282751d5)

 <p>From the above figure we can clearly observe ,the 180 degree phase shift between input and output</p>
<p>A<sub>v</sub>=V<sub>out</sub>/V<sub>in</sub></p>
<p>From graph we have v p-p voltages as</p>
<p>V<sub>in</sub>=1.349652-1.25125=0.14</p>
<p>V<sub>out</sub>1.63253-1.17119=0.46</p>
<p>A<sub>v</sub>=V<sub>out</sub>/V<sub>in</sub>=0.46/0.14=3.29 V/V</p>
<br>

 
# Ac analysis
<p>AC analysis of a differential amplifier focuses on evaluating its response to small input signals. It determines the differential gain, input and output impedance, and common-mode rejection ratio (CMRR). The amplifier amplifies the voltage difference between the two inputs while rejecting common-mode noise. Key factors influencing performance include the transistor’s transconductance and load resistance. The analysis also considers the frequency response, which is affected by parasitic capacitances. This helps in optimizing the amplifier’s performance in applications requiring noise immunity and precise signal amplification.
<p>The dc offset value is 1.3v , amplitude is 50m,and frequency is 1KHZ</p>

![Screenshot 2025-03-06 212046](https://github.com/user-attachments/assets/2f4b3f72-3e56-496e-b167-ba0f1f60a60b)
![Screenshot 2025-03-06 212107](https://github.com/user-attachments/assets/582a1a67-4886-46db-8baf-e8ebf83ac109)
<br><p>From the above figure we can note the maximum gain in db </p>
<p>A<sub>v</sub> in db=13.41db</p>

<br><Also we can calculate the gain by formula A <sub>V</sub>=20log(vout/vin)=20log(3.29)=10.33 v/v



<br>
<br>

# input and output swing
<p>Input and output swing of mos1</p>

![Screenshot 2025-03-06 212209](https://github.com/user-attachments/assets/fabe014f-c1b7-4380-a2de-0b239c4cf6c9)
<p>Input and output swing of both mosfet</p>

![Screenshot 2025-03-06 212242](https://github.com/user-attachments/assets/13d5e36b-5778-4d22-9e8a-0be19f68c47a)


# circuit 3
<p>In this circuit we have replaced the resistor with a nmos transistor and the voltage v<sub>b</sub>is 0.86v</p>
<p> V<sub>b</sub>= V<sub>t</sub>+ V<sub>p</sub> </p>
<p> V<sub>b</sub>= 0.36+0.5=0.86</p>

![Screenshot 2025-03-06 203603](https://github.com/user-attachments/assets/8a3f6595-fb82-4d58-a2da-c995627d139f)

<p>This circuit consists of three nmos transistors ,2 resistors 3 voltage sources and vdd</p>
<p>mosfets of length 180nm</p>
<p>mosfets of width 1um</p>
<p>rd of 1.81k ohm</p>
<p>vdd of 2.5v</p>
<p>vicm of each 1.3v</p>

![Screenshot 2025-03-06 204023](https://github.com/user-attachments/assets/4c64c660-ac15-406b-9db5-e3098684dcd7)


#  Dc analysis

![Screenshot 2025-03-06 203939](https://github.com/user-attachments/assets/db462d07-73b9-46ac-8c33-6b8f88335ee2)

![Screenshot 2025-03-06 204045](https://github.com/user-attachments/assets/5e629abf-c96c-453a-bd25-e682cfcc24bc)



<p>This  differential amplifgier circuit has two resistors each of 1.81k,three voltage source,vdd=2.5v</p>
<p>Mosfet length= 180nm</p>
<p>width=12.75um</p>
<p>Q point is(1.4v,0.6mA)</p>

#  Transient analysis
<p>Transient analysis of Input</p>  

![Screenshot 2025-03-06 225958](https://github.com/user-attachments/assets/2385728b-6154-41e2-aecf-a761b85ec570)

<p>Transient analysis of output</p> 

![Screenshot 2025-03-06 230039](https://github.com/user-attachments/assets/f4c31aba-d6b3-4cd0-b5e3-cef06ca30e80)

<p>Transient analysis of both input and output</p>

![Screenshot 2025-03-06 230020](https://github.com/user-attachments/assets/4f4d629d-644d-45a6-bcdc-55a0488b4a21)

<br>


![Screenshot 2025-03-06 230359](https://github.com/user-attachments/assets/19fd50b1-8d03-40bf-92fd-121690196fc7)

<p>From the above figure we can clearly observe ,the 180 degree phase shift between input and output</p>
<p>A<sub>v</sub>=V<sub>out</sub>/V<sub>in</sub></p>
<p>From graph we have v p-p voltages as</p>
<p>V<sub>in</sub>=1.708979-1.0917289=0.6172561</p>
<p>V<sub>out</sub>=1.349713-1.25023=0.099483</p>
<p>A<sub>v</sub>=V<sub>out</sub>/V<sub>in</sub>=0.099483/0.61725=6.204638V/V</p>
<br>

# Ac analysis
<p>Ac analysis of the given circuit</p>

![Screenshot 2025-03-06 230234](https://github.com/user-attachments/assets/a4810a1b-3913-4ff8-89e9-b1beaec7f0a3)

<br>

![Screenshot 2025-03-06 230308](https://github.com/user-attachments/assets/dc3e6ca8-b934-4e3f-bf5f-2b97303ce317)

<br><p>From the above figure we can note the maximum gain in db </p>
<p>A<sub>v</sub> in db=16.005db</p>

<br><Also we can calculate the gain by formula A <sub>V</sub>=20log(vout/vin)=20log(6.20463)=15.8543 v/v


# input and output swing
<p>Input and output swing of mos1</p>

![Screenshot 2025-03-06 205116](https://github.com/user-attachments/assets/7bb56303-534d-4043-a585-281416fcf1c9)

<p>Input and output swing of both mosfet</p>

![Screenshot 2025-03-06 205559](https://github.com/user-attachments/assets/f596d9d6-4dc1-4da4-b945-b3dc6fc864b1)



# Result
<p>The result of a differential amplifier is the amplified difference between the two input signals. The output voltage (V<sub>out</sub>) is calculated as:
V<sub>out</sub> = A<sub>d</sub> * (V<sub>+</sub> - V<sub>-</sub>)<br>
Where:
( A_d ) is the differential gain of the amplifier, which determines how much the difference between the inputs is amplified.<br>
( V<sub>+</sub>) is the voltage at the non-inverting input.<br>

( V<sub>-</sub>) is the voltage at the inverting input. <br>

The output is proportional to the difference between the non-inverting and inverting inputs. If the inputs are the same, the output is zero, as there is no difference to amplify.

Additionally, the amplifier ideally rejects any common-mode voltage that is present equally on both inputs. This is described by the common-mode rejection ratio (CMRR), which quantifies the amplifier's ability to reject common-mode signals and amplify only the differential signal. A high CMRR indicates the amplifier is very effective at rejecting unwanted common-mode noise.

In a practical scenario:
- If the difference between the inputs is small (e.g., millivolts), the output will be amplified according to the gain.
- If both inputs have the same voltage (i.e., no difference), the output will be zero.
  
This makes the differential amplifier particularly useful for weak signal amplification in the presence of noise, such as in instrumentation and communication systems.</p>
<br><br>
<p>1st Circuit
- DC analysis confirms MOSFET operation is in saturation .  <br>
- Transient response demonstrates proper differential operation. <br> 
- AC analysis reveals moderate gain and limited common-mode rejection.  <br></p>
<p>
2nd Circuit
- Replacing the resistor with a current source improves bias stability.  <br>
- The transient response is more stable and symmetrical  <br>
- AC analysis shows the higher gain and increased bandwidth compared to Circuit-1.  <br></p>
<p>. 
3rd Circuit
- DC analysis of circuit 3 shows that the MOSFET-based current source effectively regulates current.  <br>
- Transient response is more accurate and stable.  <br>
- AC analysis shows higher gain and improved frequency response.  <br></p>

 
# Inference
<p>In the comparative analysis of the three differential amplifier circuits, the choice of tail current implementation significantly influences performance. The first circuit, utilizing a resistor R<sub>ss</sub>, exhibits sensitivity to power supply variations and transistor mismatches, leading to potential instability in the bias current and reduced common-mode rejection ratio. This is due to the resistor's limited ability to maintain a constant current under varying conditions. In contrast, the second circuit employs an ideal current source, ensuring a stable bias current that is largely unaffected by external fluctuations, thereby enhancing both stability and CMRR.
 <br>The third circuit replaces R<sub>ss</sub> with an NMOS transistor configured as a current source with a gate voltage V<sub>b</sub></sub> of 0.76 V. This active current source provides improved performance over the resistor by offering higher output impedance, which contributes to better bias stability and CMRR. However, it may still be susceptible to variations due to transistor parameters and temperature changes. Overall, transitioning from a passive resistor to active current sources in differential amplifier designs leads to enhanced performance, with ideal current sources offering the most significant improvements. </p>
