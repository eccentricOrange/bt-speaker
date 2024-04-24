# Introduction
We have built an audio amplifier that handles bass and treble with separate drivers. The goal was to achieve this without using a pre-built amplifier like the popular TDA2030.

This report will cover the following:
1.  Design goals
2.  Overall design
3.  Filter stage
4.  Amplifier stage
5.  Challenges
6.  Schematics
7.  Simulations and expectations
8.  Results

## 2. Overall design
Our circuit is split into three main stages for each speaker:

*   **Filter:** A high-pass filter for the treble driver and a low-pass filter for the bass driver help select the frequencies at which the drivers respond best. We found good results by setting the cut-off frequency for this around 1.3 kHz.
*   **Pre-amplifier:** This is a simple voltage amplifier based on an op-amp. It provides a voltage gain of about 6, to get our signals to 6 V (peak-to-peak) for the power amplifier.
*   **Power amplifier:** This is a class AB amplifier that can deliver up to 5 W of power to each speaker. It is based on a two pairs of transistors, to get an output current of about 0.8 A.

Power is provided externally by a 24 V DC adapter, and then split to provide -12 V and 12 V.

![over-all-design](images/4-over-all-design.png)

