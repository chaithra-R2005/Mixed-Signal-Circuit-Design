# Mixed-Signal-Circuit-Design
Analysis and Implementation of a Two-Stage Op-Amp with Enhanced Stability
Design and Realization of a Two-Stage Operational Amplifier with Improved Stability

<img width="1404" height="553" alt="Screenshot 2025-11-04 075927" src="https://github.com/user-attachments/assets/c331feb7-994b-4e73-82be-d48496748512" />


A two-stage operational amplifier is a popular analog circuit used to achieve high voltage gain and a wide output voltage swing. It consists of two main stages a differential amplifier as the input stage, which offers high input impedance and initial gain, and a common-source stage that provides additional amplification to increase the overall gain.

To ensure stable performance, a Miller compensation capacitor is placed between the two stages to manage bandwidth and enhance the phase margin. This configuration offers a good balance between gain, output range, and stability, making it widely suitable for analog ICs, active filters, and signal conditioning applications. Its flexible design also allows easy optimization of parameters such as slew rate, gain-bandwidth product, and power consumption.


![spec](https://github.com/user-attachments/assets/23a5b7b3-a364-451d-b71f-09a3e0755a74)

Design Steps for Differential Amplifier Stage 

1. M1 and M2 form the differential pair which determines the gain of the amplifier.
2. The sizes of M1 and M2 are chosen to be equal (M1 = M2).
3. The tail current (I5) is split equally between M1 and M2 transistors, i.e., each gets I5/2.
4. M3 and M4 act as the active load for the differential pair.
5. For the tail NMOS transistor (M5), the VBIAS must be designed such that it provides the required tail current (I5).
6. If the desired current is known, designing VBIAS becomes straightforward.
7. M5 functions as the tail current source of the differential amplifier.


<img width="925" height="808" alt="image (1)" src="https://github.com/user-attachments/assets/d6e41e1d-c47b-4995-a34e-47b9a294af42" />


<img width="1136" height="836" alt="image (4)" src="https://github.com/user-attachments/assets/da269376-f863-4b5a-b511-3f7cfd13f9eb" />
