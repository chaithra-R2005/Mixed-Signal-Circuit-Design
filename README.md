# Mixed-Signal-Circuit-Design
Analysis and Implementation of a Two-Stage Op-Amp with Enhanced Stability
Design and Realization of a Two-Stage Operational Amplifier with Improved Stability

<img width="1404" height="553" alt="Screenshot 2025-11-04 075927" src="https://github.com/user-attachments/assets/e425deb3-829f-4bab-b478-af197912d2e0" />


A two-stage operational amplifier is a popular analog circuit used to achieve high voltage gain and a wide output voltage swing. It consists of two main stages a differential amplifier as the input stage, which offers high input impedance and initial gain, and a common-source stage that provides additional amplification to increase the overall gain.

To ensure stable performance, a Miller compensation capacitor is placed between the two stages to manage bandwidth and enhance the phase margin. This configuration offers a good balance between gain, output range, and stability, making it widely suitable for analog ICs, active filters, and signal conditioning applications. Its flexible design also allows easy optimization of parameters such as slew rate, gain-bandwidth product, and power consumption.


![spec](https://github.com/user-attachments/assets/12408571-2e71-43b4-975f-77a51f532cf2)


Design Steps for Differential Amplifier Stage 

1. M1 and M2 form the differential pair which determines the gain of the amplifier.
2. The sizes of M1 and M2 are chosen to be equal (M1 = M2).
3. The tail current (I5) is split equally between M1 and M2 transistors, i.e., each gets I5/2.
4. M3 and M4 act as the active load for the differential pair.
5. For the tail NMOS transistor (M5), the VBIAS must be designed such that it provides the required tail current (I5).
6. If the desired current is known, designing VBIAS becomes straightforward.
7. M5 functions as the tail current source of the differential amplifier.

# SCHEMATIC

This schematic represents the transistor-level design of a two-stage CMOS operational amplifier using gpdk180 models. The first stage provides differential amplification with active loads, while the second gain stage boosts overall gain and drives the output node. Compensation and load capacitors are included to ensure stability and frequency-domain performance.


<img width="817" height="826" alt="image (5)" src="https://github.com/user-attachments/assets/f24e3374-7916-485d-a207-c2b4a8fdceec" />


# Test circuit

The test circuit applies differential AC signals to evaluate the small-signal gain, bandwidth, and phase response of the designed op-amp. Supply sources and bias currents are provided to ensure correct operating points for both stages. The output node is monitored under load conditions to verify overall stability and transient behavior.



<img width="1043" height="761" alt="test_ckt" src="https://github.com/user-attachments/assets/4f325314-efaa-4480-a694-c352c0a52c38" />






