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

===============================================================================

Day 1 – PLL Theory and Lab setup_1. Introduction to PLL_Lec 1

1. PLL – to mimic multiple range of freq from reference clk wth no or negligible phase or freq noise.
2. Clk gen :
    VCO: 
     Made by inverters,
     Onchip oscillator,
     Flexible freq generation but with impure spectral i.e wide freq spectrum.
    Quarzt Crystal: 
     Pure Spectral i.e. single freq can be obtained but not flexible to generate range of freq.
3. Phase noise depicts untimely arrival of data.
4. Function of PLL is to make pure spectral of VCO.
5. PLL output: fout = n fref and constant phase difference at output clk wrt ref clk.
               This is called as lock in phase and freq with reference.
6. PLL Block Diagram

![image](https://user-images.githubusercontent.com/88277263/127831626-4271c1d4-bb57-4b36-b3ca-87a15135b784.png)

===============================================================================

Day1_2. Introduction to Phase Frequency Detector_Lec 2

![image](https://user-images.githubusercontent.com/88277263/127833964-94ccbc8f-4870-4da2-b536-9b728b23ed56.png)

Problem: for leading and lagging of output clk we have same xor output, so it will difficult to decide to make output clk fast or slow.

![image](https://user-images.githubusercontent.com/88277263/127833401-e98daf4e-f50f-42d6-b5d7-875a2a5e6c15.png)

Width of up or down signal helps in deciding of how much to make lead or lag in output clk wrt ref clk.

![image](https://user-images.githubusercontent.com/88277263/127833485-875adfd6-412e-4897-b4f1-93ec361b21ad.png)

![image](https://user-images.githubusercontent.com/88277263/127833527-9dd807c8-e746-4b31-a0b1-6b9b079a7460.png)

![image](https://user-images.githubusercontent.com/88277263/127833558-c7942911-e5df-47a9-b524-f5d09292ae61.png)

Problem: 
Dead zone : lowest phase difference or freq that PFD can detect, below which up and down signal are short and thin that is not suitable for Charge pump working, hence In this region PFD is not able to work. ( simulation performed with 1ns and 0.25ns of phase difference later in this workshop) 
This leads to phase noise in system.

===============================================================================

Day1_3. Introduction to Charge Pump_Lec 3

1. Convert digital signal (measure of phase difference at input of PFD) to Analog signal (to control VCO freq).
2. We use current steering circuit i.e. depending upon input state current will be given or drown from output cap.
3. difference in Avg time of up signal and Avg time of down signal decide the charging or discharging of output cap.
If up avg time is larger then cap will be charging and vicevera.

![image](https://user-images.githubusercontent.com/88277263/127834655-fe38d48d-1029-4f8e-96e6-efeb56c9e688.png)

4. Loop filter:

![image](https://user-images.githubusercontent.com/88277263/127834767-b0bff1db-277c-40e2-8580-151fdd526ef6.png)

Cload = C1/10

Loop filter BW = 1/RC’ = fout/10     C’ = C1||Cload

===============================================================================

Day1_4. Introduction to VCO and Frequency Divider_Lec 4

1. VCO 

   Ring oscillator is onchip oscillator but with fix freq .

![image](https://user-images.githubusercontent.com/88277263/127835455-c55caa90-0619-4744-8d20-51ff2b58815c.png)

   To make flexible freq in ring oscillator we will vary SUPPLY current as per need of the time to rise and fall of signal.

![image](https://user-images.githubusercontent.com/88277263/127835525-40e8daf6-cee9-4748-b0fd-d11f588ce730.png)

2 Freq Division:

1. Toggle ff divide the input clk by 2 . 

![image](https://user-images.githubusercontent.com/88277263/127835599-c69b54ba-f075-4ec2-a37b-3ae25b914963.png)

2. For more Division need to cascade the Toggle FF as below:

![image](https://user-images.githubusercontent.com/88277263/127835660-56e017ae-e514-4181-b22e-01dacef21c37.png)

PLL Terms:
1. Lock Range: After Lock is done , range of freq PLL can follow ref clk 
2. Capture Range: From unlock condition to Lock condition range of freq PLL can lock.
                  
                  CR<LR
                  Loop filter BW effects CR.
3. Settling time: Time taken from unlock state to locked.
                  
                  Depends on charge pump time to reach it’s stable value.

===============================================================================

Day1_5. Tool setup and design flow_Lec 5

1. ngspice = ckt simulator
2. magic = layout design 
3. sky130nm.tech technology file for magic 
4. Flow: 
            1. Ckt design
            2. Prelayout sim
            3. Layout
            4. Parasitic extrc
            5. Postlayout sim

===============================================================================

Day1_6. Introduction to PDK, specifications and pre-layout circuits_Lec 6

1. Open Source Google-Skywater 130nm
2. available pdk are:
                                    
                                    io = input output
                                    pr = primitive (spice)   we use this type  
                                    sc = standard cell
                                    hd = high density
                                    hs = high speed
                                    lp = low power
                                    hdll = high density low leakage
  
 3 specs:
                                    
                                    TT corner
                                    1.8V VDD
                                    Room temp 27C
                                    VCO (VCO use as PLL with external control) and PLL mode
                                    Input freq 5MHz to 12.5MHz
                                    8x Multipier
                                    Jitter RMS (RMS of variation in period or phase noise) < 20ns  (nearly 10ns)
                                    50% Duty Cycle
  
 
 4. Circuits:
 
 ![image](https://user-images.githubusercontent.com/88277263/127838308-cefa2a94-77e9-49fe-adc4-e7f7811acfd6.png)

===============================================================================

Day1_7. Circuit design simulation tool - Ngspice Setup_Lec 7

1. Need 4 files to simulate included in sky130.lib:

                                            1. sky130_fd_pr__pfet_01v8__tt.pm3.spice
                                            3. sky130_fd_pr__nfet_01v8__tt.pm3.spice
                                            4. lod.spice
                                            5. invariant.spice
2. These files are in spice_lib folder from there path is to copied in sky130.lib.
3. Reference: avsdpll_1v8 (path is in reference)
4. pdk: google/skywater-pdk -> sky130_fd_pr

===============================================================================

Day1_8. Layout design tool - Magic Setup_Lec 8

Tech used: sky130A.tech 

It is included in the work directory.

===============================================================================














