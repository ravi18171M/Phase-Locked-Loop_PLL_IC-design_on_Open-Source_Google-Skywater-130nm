# Phase-Locked Loop(PLL) IC design on Open-Source Google-Skywater 130nm
![image](https://user-images.githubusercontent.com/88277263/127781279-485d7b13-fd40-4d03-9192-d7a31bf04769.png)
31 July and 1 August 2021

Reference: https://github.com/lakshmi-sathi/avsdpll_1v8.git

Add hyperlink

Content :

Day 1 – PLL Theory and Lab setup
1.	Introduction to PLL
2.	Introduction to Phase Frequency Detector
3.	Introduction to Charge Pump
4.	Introduction to VCO and Frequency Divider
5.	Tool setup and design flow
6.	Introduction to PDK, specifications and pre-layout circuits
7.	Circuit design simulation tool - Ngspice Setup
8.	Layout design tool - Magic Setup
Day 2 – PLL Labs and post-layout simulations
1.	PLL components circuit design
2.	PLL components circuit simulations
3.	Steps to combine PLL sub-circuits and PLL full design simulation
4.	Troubleshooting steps
5.	Layout design
6.	Layout Walkthrough
7.	Parasitics extraction
8.	Post Layout simulations
9.	Steps to combine layouts
10.	Tapeout theory
11.	Tapeout labs



==========================================================================================================

Day 1 – PLL Theory and Lab setup

1. Introduction to PLL

Lec 1

1. PLL – to mimic multiple range of freq from reference clk wth no or negligible phase or freq noise.
2. Clk gen :
VCO: 
Made by inverters
Onchip oscillator
Flexible freq generation but with impure spectral i.e wide freq spectrum.

Quarzt Crystal: 
Pure Spectral i.e. single freq can be obtained but not flexible to generate range of freq.
3. Phase noise depicts untimely arrival of data.
4. Function of PLL is to make pure spectral of VCO.
5. PLL output: fout = n fref and constant phase difference at output clk wrt ref clk.
This is called as lock in phase and freq with reference.
6. PLL Block Diagram
 


==========================================================================================================

Day1
2. Introduction to Phase Frequency Detector

Lec 2
1. 
 
Problem: for leading and lagging of out we have same xor output, so it will difficult to decide to make out fast or slow.
 
Width of up or down signal helps in deciding of how much to make lead or lag in output clk wrt ref clk.

 
 

 
Problem: 
Deadzone : lowest phase difference or freq that PFD can detect, below which up and sown signal are short and thin that is not suitable for Charge pump working, hence In this region PFD is not able to work. (simulation performed with 1ns and 0.25ns of phase difference later in this workshop) 
This leads to phase noise in system.










==========================================================================================================


