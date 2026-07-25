# Power Electronics Converter Simulation

This repository contains MATLAB/Simulink simulations of power electronic converters and electric drive systems developed as part of my Electrical Engineering coursework at Delhi Technological University.

Software Used

- MATLAB
- Simulink
- Simscape Electrical
- Microsoft Visio

---

## Single Phase Fully Controlled Rectifier (R Load)

### Circuit Parameters

| Parameter | Value |
|-----------|-------|
| AC Source Voltage | 220 V |
| Supply Frequency | 50 Hz |
| Firing Angle | 60° |
| Load Resistance | 1 Ω |

### Circuit Diagram

<img src="image2.png" width="45%">
<img src="image3.jpeg" width="45%">

### Output Waveforms

<img src="image4.jpeg" width="75%">

### THD Analysis

<img src="image5.jpeg" width="65%">

### Output Power

<img src="image6.jpeg" width="65%">

### Observation

The load current follows the output voltage because the load is purely resistive. Since there is no energy storage element, current becomes zero at the end of every half cycle. Increasing the firing angle reduces the average output voltage and output power.
# Power Electronics Converter Simulation

This repository contains MATLAB/Simulink simulations of power electronic converters and electric drive systems developed as part of my Electrical Engineering coursework at Delhi Technological University.

Software Used

- MATLAB
- Simulink
- Simscape Electrical
- Microsoft Visio

---

## Single Phase Fully Controlled Rectifier (R Load)

### Circuit Parameters

| Parameter | Value |
|-----------|-------|
| AC Source Voltage | 220 V |
| Supply Frequency | 50 Hz |
| Firing Angle | 60° |
| Load Resistance | 1 Ω |

### Circuit Diagram

<img src="image2.png" width="45%">
<img src="image3.jpeg" width="45%">

### Output Waveforms

<img src="image4.jpeg" width="75%">

### THD Analysis

<img src="image5.jpeg" width="65%">

### Output Power

<img src="image6.jpeg" width="65%">

### Observation

The load current follows the output voltage because the load is purely resistive. Since there is no energy storage element, current becomes zero at the end of every half cycle. Increasing the firing angle reduces the average output voltage and output power.
# DC-DC Buck Converter (R Load)

The buck converter was designed to step down a 200 V DC input to 150 V using a switching duty cycle of 0.75. The simulation was performed to study the output voltage, current and converter characteristics under a resistive load.

### Circuit Parameters

| Parameter | Value |
|-----------|-------|
| Input Voltage | 200 V |
| Output Voltage | 150 V |
| Duty Cycle | 0.75 |
| Filter Inductance | 380 μH |
| Filter Capacitance | 411 μF |
| Load Resistance | 20 Ω |

### Circuit Diagram

<img src="image28.png" width="45%">
<img src="image29.jpeg" width="45%">

### Output Waveforms

<img src="image30.png" width="45%">
<img src="image31.png" width="45%">

### Output Power

<img src="image32.jpeg" width="65%">

### Observation

The converter successfully stepped down the input voltage from 200 V to approximately 150 V, matching the theoretical relation \(V_{out}=D \times V_{in}\). The selected inductor and capacitor values reduced current and voltage ripple, while the output remained stable under steady-state operation.

---

# DC-DC Buck Converter (DC Motor Load)

The buck converter was also tested with a separately excited DC motor to study its performance as a DC chopper drive.

### Circuit Parameters

| Parameter | Value |
|-----------|-------|
| Input Voltage | 200 V |
| Filter Inductance | 380 μH |
| Filter Capacitance | 411 μF |
| Motor Rating | 5 HP |
| Rated Armature Voltage | 240 V |
| Rated Speed | 1750 RPM |
| Field Voltage | 150 V |

### Circuit Diagram

<img src="image34.jpeg" width="70%">

### Output Waveforms

<img src="image35.jpeg" width="70%">

<img src="image36.jpeg" width="70%">

### Effect of Duty Cycle on Armature Current

<img src="image37.png" width="65%">

### Effect of Duty Cycle on Field Current

<img src="image38.jpeg" width="65%">

### Effect of Duty Cycle on Torque

<img src="image39.png" width="65%">

### Effect of Duty Cycle on Speed

<img src="image40.jpeg" width="65%">

### Effect of Duty Cycle on Output Power

<img src="image41.jpeg" width="65%">

### Effect of Duty Cycle on Output Voltage

<img src="image42.jpeg" width="65%">

### Observation

The buck converter operated as a Class-A DC chopper, providing smooth speed control by varying the duty cycle. Increasing the duty cycle increased the average armature voltage, resulting in higher motor speed and torque. The combined effect of the filter and motor inductance reduced current ripple, producing stable motor operation throughout the simulation.

---
# Single Phase Full Bridge Inverter (R Load)

The single-phase full bridge inverter was simulated using both Bipolar PWM and Unipolar PWM techniques. The objective was to compare the output voltage, output current and switching characteristics for a purely resistive load.

### Circuit Parameters

| Parameter | Value |
|-----------|-------|
| DC Source Voltage | 100 V |
| Fundamental Frequency | 50 Hz |
| Carrier Frequency | 1000 Hz |
| Modulation Index | 0.8 |
| Load Resistance | 10 Ω |

### Circuit Diagram

<img src="image43.jpeg" width="70%">

---

## Bipolar PWM

### Simulink Model

<img src="image44.jpeg" width="70%">

### Gate Signals

<img src="image45.jpeg" width="70%">

### Output Voltage

<img src="image46.png" width="70%">

### Output Current

<img src="image47.png" width="70%">

### Observation

In Bipolar PWM, the output voltage switches directly between +Vdc and -Vdc, producing a two-level output waveform. Since the load is purely resistive, the output current follows the voltage waveform. The inverter operates with a simple switching strategy but produces relatively higher harmonic content.

---

## Unipolar PWM

### Simulink Model

<img src="image48.jpeg" width="70%">

### Gate Signals

<img src="image49.jpeg" width="70%">

### Output Voltage

<img src="image50.png" width="70%">

### Output Current

<img src="image51.jpeg" width="70%">

### Observation

In Unipolar PWM, the output voltage alternates between +Vdc, 0 and -Vdc, resulting in a three-level waveform. Compared with Bipolar PWM, the output contains lower harmonic distortion and smoother current, making it more suitable for practical inverter applications.

---

# Single Phase Full Bridge Inverter (RL Load)

The inverter was next simulated with an RL load to observe the effect of inductance on output current and waveform quality.

### Circuit Parameters

| Parameter | Value |
|-----------|-------|
| DC Source Voltage | 100 V |
| Fundamental Frequency | 50 Hz |
| Carrier Frequency | 1000 Hz |
| Modulation Index | 0.8 |
| Load Resistance | 20 Ω |
| Load Inductance | 10 mH |

### Circuit Diagram

<img src="image52.jpeg" width="70%">

---

## Bipolar PWM

### Simulink Model

<img src="image53.jpeg" width="70%">

### Output Voltage

<img src="image54.png" width="70%">

### Output Current

<img src="image55.jpeg" width="70%">

### Observation

The inductive load smooths the output current and delays its response with respect to the voltage waveform. Although the output voltage remains unchanged, the current ripple is significantly reduced because of the energy stored in the inductor.

---

## Unipolar PWM

### Simulink Model

<img src="image56.jpeg" width="70%">

### Output Voltage

<img src="image57.png" width="70%">

### Output Current

<img src="image58.jpeg" width="70%">

### Observation

The RL load with Unipolar PWM produces a smoother current waveform than Bipolar PWM. The three-level output voltage reduces harmonic distortion and improves the quality of power delivered to the load without increasing the switching frequency of the devices.

---# Single Phase PWM Inverter with Induction Motor Load

The inverter was finally tested with a single-phase induction motor to compare the performance of Bipolar PWM and Unipolar PWM under motor loading conditions.

### Circuit Parameters

| Parameter | Value |
|-----------|-------|
| DC Source Voltage | 100 V |
| Fundamental Frequency | 50 Hz |
| Carrier Frequency | 1000 Hz |
| Modulation Index | 0.8 |
| Motor Type | Capacitor-Start Single Phase Induction Motor |
| Motor Rating | 0.25 HP |
| Rated Voltage | 110 V |
| Rated Frequency | 60 Hz |

---

## Bipolar PWM

### Circuit Diagram

<img src="image59.jpeg" width="70%">

### Simulink Model

<img src="image60.jpeg" width="70%">

### Gate Signals

<img src="image45.jpeg" width="70%">

### Output Voltage

<img src="image61.png" width="70%">

### Motor Characteristics

<img src="image62.jpeg" width="70%">

### Observation

The motor starts successfully and reaches a steady operating speed. The output voltage alternates between +Vdc and -Vdc, resulting in higher harmonic content. Torque and stator current show noticeable ripple because of the switching pattern used in Bipolar PWM.

---

## Unipolar PWM

### Circuit Diagram

<img src="image59.jpeg" width="70%">

### Simulink Model

<img src="image63.jpeg" width="70%">

### Gate Signals

<img src="image49.jpeg" width="70%">

### Output Voltage

<img src="image64.png" width="70%">

### Observation

The motor reaches nearly the same steady-state speed as in Bipolar PWM, but with smoother current and reduced torque ripple. The three-level output voltage improves waveform quality and reduces harmonic distortion, making Unipolar PWM a better choice for inverter-fed motor drives.

---

# Conclusion

This repository demonstrates the simulation and analysis of commonly used power electronic converters and electric drive systems using MATLAB/Simulink.

The following systems were modeled and analyzed:

- Single Phase Fully Controlled Rectifier with R, RL and RLE loads
- DC Motor Drive
- DC-DC Buck Converter with Resistive and Motor loads
- Single Phase Full Bridge Inverter using Bipolar and Unipolar PWM
- Single Phase PWM Inverter feeding an Induction Motor

The simulations were used to study converter operation, waveform characteristics, harmonic performance, and the effect of firing angle, duty cycle, and PWM techniques on system performance. The results also demonstrate the influence of different load types on current conduction, ripple, output voltage, and motor characteristics.

All circuit models were developed using MATLAB/Simulink and Simscape Electrical, while circuit schematics were prepared using Microsoft Visio.
