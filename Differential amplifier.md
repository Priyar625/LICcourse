## Experiment-3 : Design and Analysis of MOS differential amplifier circuit


## theory

Differential amplifiers apply gain not to one input signal but to the difference between two input signals. This means that a differential amplifier naturally eliminates noise or interference that is present in both input signals.
Differential amplification also suppresses common-mode signals—in other words, a DC offset that is present in both input signals will be removed, and the gain will be applied only to the signal of interest (assuming, of course, that the signal of interest is not present in both inputs). This is particularly advantageous in the context of IC design because it eliminates the need for bulky DC-blocking capacitors.
The subtraction that occurs in a differential pair makes it easy to incorporate the circuit into a negative-feedback amplifier

![Image](https://github.com/user-attachments/assets/561bdd8c-9581-438d-99c2-5fdfc97dbf0f)

DC Analysis

The given circuit is a differential amplifier using MOSFETs. significance of each component:

1. Q1 & Q2 (MOSFETs): These two transistors form the differential pair. They compare the input signals VIN1 and VIN2 and amplify the difference between them.

2. R1 and R2 (Load Resistors): These resistors convert the drain currents of Q1 and Q2 into output voltages V_OUT1 and V_OUT2. They play a role in setting the gain of the amplifier.

3. I_BIAS (Current Source): This component provides a constant current, which is split between Q1 and Q2 depending on their gate voltages. It stabilizes the operation and determines the total current flowing through the circuit.

4. Power Supply (+V and -V): The positive supply voltage (+V) powers the drain terminals of Q1 and Q2, while the negative voltage (-V) is used for the current source.

5. V_IN1 and V_IN2 (Input Signals): These are the differential input signals applied to the gates of Q1 and Q2. The circuit amplifies the voltage difference between these inputs.

6. V_OUT1 and V_OUT2 (Output Signals): These nodes provide the amplified differential output signals.

Overall Function
This differential amplifier is used in applications such as:
- Amplifying small differential signals while rejecting common-mode noise.
- Serving as an input stage in operational amplifiers.
- Acting as a comparator in analog circuits.


Let’s determine the biasing conditions of this circuit when both inputs are grounded.

![Image](https://github.com/user-attachments/assets/daca79f0-f2ba-491f-b97f-1de4b7077244)

The sum of the two drain currents ID1 and ID2 must equal IBIAS. We also know that the two drain currents are equal because, in this idealized analysis, both halves of the circuit are identical. Thus,

![Image](https://github.com/user-attachments/assets/d99e4864-8f3b-499f-b912-ece831a8f00d)

 Let’s assume for the moment that the transistors are in saturation. The equation for saturation-mode drain current is the following:

 
 ![Image](https://github.com/user-attachments/assets/f8287929-7685-4dfe-b68a-580a1cab1b56)

## Aim of the experiment: Design and analyse differential amplifier circuit for the following specifications:

## design question
VDD= 2.2V , P<=2.2mW , Vincm =1.2V , Vocm = 1.25V , Vp = 0.4V Perform: DC analysis, transient analysis, frequency response and extract the parameters.
solution: we know that P= VddIss 

Iss = P/Vdd = 2.2mW/2.2V = 1mA

Iss = 1mA

ID = Iss/2 = 1m/2 =0.5mA

ID = 0.5mA

(from VDD = IDRD + Vocm)

RD = (VDD - Vocm)/ID 

RD = (2.2-1.25)/0.5m = 1.9Kohm

RD = 1.9Kohm

Rss = Vp/Iss = 0.4/1m = 400ohm

 Rss = 400ohm

## circuit diagram:

## A)With Resistor Rss

![Image](https://github.com/user-attachments/assets/c5af35e1-b7e7-46fb-b2f6-1d6e87a24baa)


## B) Resistor Rss replaced with current source Iss

![Image](https://github.com/user-attachments/assets/dc943035-c6b9-4506-abb8-ec60469c6384)


## C) Resistor Rss replaced with NMOSFET


![Image](https://github.com/user-attachments/assets/ff1b2bb3-a736-4da8-a325-e6125d9fa483)


## Design and analysis

## A) With Resistor Rss:

The circuit is intended to eliminate common-mode signals.

It amplifies only the differential signal between VinCM1 and VinCM2.

The output voltage range is restricted by the supply voltage (VDD) and the transistor's saturation conditions.

## 1.DC Analysis- To fix the operating point (Q-point):

![Image](https://github.com/user-attachments/assets/c5af35e1-b7e7-46fb-b2f6-1d6e87a24baa)

![Image](https://github.com/user-attachments/assets/629f36cc-e80f-4b29-920b-79661ab7267c)

![Image](https://github.com/user-attachments/assets/8a77f448-3183-4958-b585-f9eddcffca64)

Length( of M1 and M2) = L = 180.1nm

Width ( of M! and M2) = W = 6.415um

for mosfet M1:

VoCM1 = 1.25v

ViCM1 = 1.2V

Id(M1) = 0.4999 mA

Vtn =  0.495v

VGS = 1.2 - 0.4 = 0.8v

VDD = IdRd + VDS +Vp

VDS = 2.2 - 0.4 - 0.95

VDS = 0.85 V

for mosfet M2:

VoCM2 = 1.25v

ViCM2 = 1.2V

Id(M2) = 0.4999 mA

Vtn =  0.495v

VGS = 1.2 - 0.4 = 0.8v

VDD = IdRd + VDS +Vp

VDS = 2.2 - 0.4 - 0.95

VDS = 0.85 V


To verify the mosfets are in saturation region : VGD <= VTn

(1.2V -1.25V) <=  0.495V

-0.05V <=  0.495V

and VDS >= Vov

(1.25 - 0.4) >= (1.2 - 0.4) -  0.495

0.85V >= 0.305Vv

Therefore mosfets are in saturation region .

The Q-points of both the mosfets(M1 and M2) are (0.85V, 0.5mA)

 If the value of the vicm increase from the Vincm to 1.3V from 1.2V (0.1V increase), these are the respective changes.


![Image](https://github.com/user-attachments/assets/96d25d51-dce2-4a05-8bcb-5291352086a6)


![Image](https://github.com/user-attachments/assets/b9bafbd5-63b5-4c97-9675-c1ea1067817e)

so, there is a slight variation in the Q-point as (0.6456V, 0.576mA)

## Transient Analysis: 

In LTSpice, transient analysis is used to model how a circuit responds over time to varying inputs like pulses, sine waves, or step functions. 
This type of analysis is essential in high-speed applications, as it helps assess important factors such as rise time, fall time, and propagation delay, which determine the amplifier’s ability to handle fast signals.
It also examines how the MOSFET reacts to rapid changes in input voltage and load conditions.

nput waveform and output waveform

![Image](https://github.com/user-attachments/assets/0716736e-445c-43b4-af4a-1f2dd032573f)

![Image](https://github.com/user-attachments/assets/5fc4bd2c-2757-4479-a767-5a743a7565f2)

From the graph ,we can observe the 180 degree phase shift in the output signal and the output voltage (at Vocm node) is amplified .

 Gain(Av) = Vout_peak/Vin_peak

= 0.377/0.099 = 3.808V/V

From calculations, gm = 2ID/Vov = (2* 0.5m)/ (0.8 - 0.495) = 3.278m 

Rout = Rd = 1.9 kohm

Overall gain :Av = gm * Rd

Av= 3.278m * 1.9K = 6.22V/V.

## 3. AC analysis:

The AC analysis in LTSpice is used to analyze the frequency response of an amplifier, including parameters such as gain, bandwidth, and phase shift.
In this analysis, the MOSFET is modeled as a linear small-signal amplifier, where the drain current responds proportionally to small changes in gate voltage.
By applying a small-signal AC input, this analysis helps us understand how the circuit amplifies signals and how it performs across different frequencies.


![Image](https://github.com/user-attachments/assets/d20816fb-ac4d-4f22-b983-fb3e910ba630)

From the graph , the gain in dB scale is 12.125dB - 3dB = 9.125dB

4. To calculate maximum input swing and output swing
Vincm_min = Vth1 + Vov = 0.495 + 0.4 = 0.895V

Vincm_max = VDD -(RD*Iss)/2 + Vth = 2.2 -(1.9k * 1m)/2 + 0.495 = 1.745V

Therefore Vincm = (Vincm_min + Vincm_max)/2 = 1.32V

and Vocm_min = Vov1 + Vov2 = (0.8 - 0.495) + 0.4 = 0.705V

Vocm_max = VDD - IDRD = 2.2 -(0.5m* 1.9K) = 1.25V

Therefore Vocm = (Vocm_min + Vocm_max)/2 = 0.977V

![Image](https://github.com/user-attachments/assets/354c3372-f00a-4c2d-8027-dd2b26ac22f3)



Here the dc offset voltage is set to 1.4V, input amplitude to 500mV, to observe the clipped output waveform.

The Vo_pp (of clipped waveform) was 1.533V

## B) Resistor Rss replaced with current source Iss:


Using an active current source in place of R3 enhances both the gain and the Common-Mode Rejection Ratio (CMRR). 
The overall performance of the circuit is improved when R3 is replaced with an active current source.


![Image](https://github.com/user-attachments/assets/d7fc5df6-5a6b-4199-9a8e-05766cf23acb)


![Image](https://github.com/user-attachments/assets/b45daff0-f1f0-4484-a09b-7843cefa1205)


## 1.DC analysis - To fix the operating point (Q-point):

Mosfet aspect ratio was same ie, L= 180.1nm, W = 6.415um

for mosfet  M1 & M2:

VoCM = 1.25v

ViCM = 1.2V

Id= 0.5 mA

Vtn =  0.495v

VGS = 1.2 - 0.4 = 0.8v

VDD = IdRd + VDS +Vp

VDS = 2.2 - 0.4 - 0.95

VDS = 0.85 V

To verify the mosfets are in saturation region : VGD <= VTn

(1.2V -1.25V) <=  0.495V

-0.05V <=  0.495V

and VDS >= Vov

(1.25 - 0.4) >= (1.2 - 0.4) -  0.495

0.85V >= 0.305Vv

Verified the mosfets are in saturation region by : VGD <=Vtn and VDS >= Vov.

The Q-point of both the mosfets are (0.85V, 0.5mA).


## 2. Transient analysis:
Performed the transient analysis keeping the sinusoidal voltage signal DC offset as 1.2V, amplitude 50mV , frequency 1KHz and the AC amplitude as 1V. In the configure analysis, select stop time as 5ms.

![Image](https://github.com/user-attachments/assets/db2a9ac2-22b7-437d-b5f6-cc3e2d013010)

![Image](https://github.com/user-attachments/assets/1e84869b-fb4b-46db-98ca-8c2746d0a5be)


From the graph ,we can observe the 180 degree phase shift in the output signal and the output voltage (at Vocm node) is amplified .

Input voltage amplitude given was 50mV.

From the graph,

Overall Gain(Av) = Vout_peak/Vin_peak

=0.3984/0.09916 = 4.01V/V

From calculations, gm = 2ID/Vov = (2* 0.5m)/ (0.8 - 0.495) = 3.278m

Rout = Rd = 1.9 Kohm

Overall gain :Av = gm * Rd

= 3.278m * 1.9K = 6.22V/V.

## 3.AC analysis:

![Image](https://github.com/user-attachments/assets/78503986-a7e7-4e81-9ca0-2eed3ec6be68)

From the graph , the gain in dB scale is 12.129dB - 3dB = 9.129dB

4. To calculate maximum input swing and output swing
As calculated earlier,

Vincm = (Vincm_min + Vincm_max)/2 = 1.32V

and Vocm = (Vocm_min + Vocm_max)/2 = 0.977V

Input and output at M1

![Image](https://github.com/user-attachments/assets/8f4a360b-3068-4f89-90c5-5449509460b0)

Input and output at both M1 and M2

![Image](https://github.com/user-attachments/assets/2de31da5-593b-40a4-8925-47afb3ef5b5d)


Here the dc offset voltage is set to 1.4V, input amplitude to 500mV, to observe the clipped output waveform.

The Vo_pp (of clipped waveform) was 1.5901V


## C) Resistor Rss replaced with NMOSFET:

When the tail resistor (R3) is replaced with an NMOS current source, the differential amplifier shows better performance, including higher gain, a wider output swing, and improved common-mode rejection. 
This configuration offers enhanced biasing and stability, outperforming a simple resistor or an ideal current source.

## 1.DC analysis - To fix the operating point (Q-point):

![Image](https://github.com/user-attachments/assets/d0ca7d7e-14a1-4ab2-bcfc-c58da89a254d)



![Image](https://github.com/user-attachments/assets/3d28b4e4-899d-4bbd-8c40-a745ab575743)



![Image](https://github.com/user-attachments/assets/bb9c7356-80f0-4ade-93c8-f49e5371f356)



Here the bias voltage(gate voltge of M3) must be calculated to ensure that the mosfet is in saturation region.

It is given by : Vb = Vp + Vtn 

Vb = 0.4V + 0.49V = 0.89V


Verified the mosfets are in saturation region by : VGD <=Vtn and VDS >= Vov.

Therefore Q-point of M3 is (0.4V, 1mA) Q-point of M1 and M2 is (0.85V, 0.5mA)


## Transient analysis:
Performed the transient analysis keeping the sinusoidal voltage signal DC offset as 1.2V, amplitude 50mV , frequency 1KHz and the AC amplitude as 1V. In the configure analysis, select stop time as 5ms.

Input and output waveforms at M1

![Image](https://github.com/user-attachments/assets/7a29fc35-d52c-477d-b9f7-0709567fc18a)



Input and output waveforms at M1 and M2

![Image](https://github.com/user-attachments/assets/14218f95-b7db-4bea-a769-28bd1996e218)


From the graph ,we can observe the 180 degree phase shift in the output signal and the output voltage (at Vocm node) is amplified

Input voltage amplitude given was 50mV.

From the graph,

Overall Gain(Av) = Vout_peak/Vin_peak = 0.3979V/0.099V = 4.019V/V

From calculations, gm = 2ID/Vov = (2* 0.5m)/ (0.8 - 0.495) = 3.278m

Rout = Rd = 1.9Kohm

Overall gain :Av = gm * Rd

= 3.278m * 1.9K = 6.22V/V

## 3.AC analysis:


![Image](https://github.com/user-attachments/assets/773fcc15-0858-4acb-9ab9-7cb532a85a9c)


rom the graph , the gain in dB scale is 12.129dB - 3dB = 9.129dB

To calculate maximum input swing and output swing
As calculated earlier,

Vincm = (Vincm_min + Vincm_max)/2 = 1.32V

and Vocm = (Vocm_min + Vocm_max)/2 = 0.977V

Input and output at M1

![Image](https://github.com/user-attachments/assets/e4d1093b-84ba-401b-8d72-437543fcc515)


Input and output at both M1 and M2

![Image](https://github.com/user-attachments/assets/40b98915-9e61-46d8-8df7-9256ee1e4bb7)


Here the dc offset voltage is set to 1.4V, input amplitude to 500mV, to observe the clipped output waveform.

The Vo_pp (of clipped waveform) was 1.617V.


## Inference: 


With Resistor (Rss) as Tail Current Source:

Moderate Differential Gain: The differential gain is limited by the resistor (Rss) because the tail current is fixed and affected by the resistance value. A resistor in the tail limits the current that flows through the differential pair, reducing the overall amplification.

Reason: The resistor in the tail does not actively control the current, so its value directly impacts the current flowing through the differential pair, limiting the overall gain.

Reduced Output Voltage Swing:  
The output swing is constrained due to the voltage drop across the tail resistor (Rss). As the output voltage approaches the supply voltage, the current through the resistor drops, reducing the available headroom for the output signal.

Reason: The voltage drop across Rss eats up a significant portion of the available headroom, which limits how far the output can swing before reaching supply limits.

Low Common-Mode Rejection Ratio (CMRR):  The CMRR is low because the tail resistor provides a low impedance, which allows common-mode signals to affect both sides of the differential pair in a similar manner.

Reason: The low impedance of the resistor doesn’t sufficiently isolate the differential pair from common-mode signals. Therefore, both the positive and negative inputs are more likely to be affected by common-mode interference, reducing the CMRR.

 With  Current Source (Iss) as Tail Current Source:

Higher Differential Gain:  
  The ideal current source provides a constant tail current, improving differential gain by maintaining a steady current that flows through the differential pair, resulting in greater amplification.

Reason: The constant tail current ensures that the differential pair operates within its optimal region. This enables the circuit to amplify signals more efficiently, resulting in higher gain.

Improved Output Voltage Swing:  
  An ideal current source increases the available headroom for the output swing by maintaining a constant current, regardless of fluctuations in the load or voltage at the output.

  Reason: The ideal current source doesn’t experience voltage drops like the resistor does. Thus, more of the supply voltage is available for the output swing, allowing the signal to swing more freely.

 Higher CMRR:  
  The ideal current source has high impedance, which helps isolate the differential pair from common-mode signals, improving the CMRR.

  Reason: The high impedance of the ideal current source ensures that the tail current remains unaffected by fluctuations in the power supply or common-mode signals. This results in better rejection of common-mode interference, leading to a higher CMRR.



With NMOS Current Source as Tail Current Source:

Highest Differential Gain:  
  The NMOS current source provides an active current source with high impedance. This setup allows the differential pair to operate at its maximum potential, resulting in the highest differential gain.

  Reason: The high impedance of the NMOS current source minimizes current variations, ensuring that the differential pair is consistently biased for maximum amplification. The active current source optimizes the current flow, leading to the highest possible differential gain.

Best Output Voltage Swing:  
  The NMOS current source minimizes the voltage drop in the tail, which allows the output swing to be the widest. This minimizes voltage loss, keeping more of the supply voltage available for the output.

  Reason: Because the NMOS current source is an active device with high impedance, it doesn't drop as much voltage across itself as a resistor would. This leaves more room for the output signal to swing before hitting supply limits.


Maximum CMRR:  
  The NMOS current source provides the highest CMRR because it offers superior isolation from supply variations and common-mode signals.

  Reason: The NMOS current source, being an active component with high impedance, better isolates the differential pair from power supply fluctuations and common-mode interference. This isolation leads to the best common-mode rejection performance, ensuring that the circuit rejects unwanted signals more effectively.


Summary of Reasons:

- Resistor (Rss): Limits current flow, reduces output swing, and provides low impedance, making it less effective at rejecting common-mode signals.
- Ideal Current Source: Provides a constant current, improving gain, output swing, and CMRR due to its high impedance.
- NMOS Current Source: Acts as an active high-impedance source, leading to the best performance in terms of differential gain, output swing, and common-mode 
  rejection, thanks to better biasing and isolation from interference.


