# Phase-Locked Loop(PLL) IC design on Open-Source Google-Skywater 130nm
![image](https://user-images.githubusercontent.com/88277263/127781279-485d7b13-fd40-4d03-9192-d7a31bf04769.png)
31 July and 1 August 2021

## Content :
[Day 1 – PLL Theory and Lab setup](https://github.com/ravi18171M/Phase-Locked-Loop_PLL_IC-design_on_Open-Source_Google-Skywater-130nm/blob/main/README.md#day-1--pll-theory-and-lab-setup_1-introduction-to-pll_lec-1) 

- [1.	Introduction to PLL](https://github.com/ravi18171M/Phase-Locked-Loop_PLL_IC-design_on_Open-Source_Google-Skywater-130nm/blob/main/README.md#day-1--pll-theory-and-lab-setup_1-introduction-to-pll_lec-1)

[2.	Introduction to Phase Frequency Detector](https://github.com/ravi18171M/Phase-Locked-Loop_PLL_IC-design_on_Open-Source_Google-Skywater-130nm/blob/main/README.md#day1_2-introduction-to-phase-frequency-detector_lec-2)

[3.	Introduction to Charge Pump](https://github.com/ravi18171M/Phase-Locked-Loop_PLL_IC-design_on_Open-Source_Google-Skywater-130nm/blob/main/README.md#day1_3-introduction-to-charge-pump_lec-3)

[4.	Introduction to VCO and Frequency Divider](https://github.com/ravi18171M/Phase-Locked-Loop_PLL_IC-design_on_Open-Source_Google-Skywater-130nm/blob/main/README.md#day1_4-introduction-to-vco-and-frequency-divider_lec-4)

[5.	Tool setup and design flow](https://github.com/ravi18171M/Phase-Locked-Loop_PLL_IC-design_on_Open-Source_Google-Skywater-130nm/blob/main/README.md#day1_5-tool-setup-and-design-flow_lec-5)

[6.	Introduction to PDK, specifications and pre-layout circuits](https://github.com/ravi18171M/Phase-Locked-Loop_PLL_IC-design_on_Open-Source_Google-Skywater-130nm/blob/main/README.md#day1_6-introduction-to-pdk-specifications-and-pre-layout-circuits_lec-6)

[7.	Circuit design simulation tool - Ngspice Setup](https://github.com/ravi18171M/Phase-Locked-Loop_PLL_IC-design_on_Open-Source_Google-Skywater-130nm/blob/main/README.md#day1_7-circuit-design-simulation-tool---ngspice-setup_lec-7)

[8.	Layout design tool - Magic Setup](https://github.com/ravi18171M/Phase-Locked-Loop_PLL_IC-design_on_Open-Source_Google-Skywater-130nm/blob/main/README.md#day1_8-layout-design-tool---magic-setup_lec-8)




[Day 2 – PLL Labs and post-layout simulations](https://github.com/ravi18171M/Phase-Locked-Loop_PLL_IC-design_on_Open-Source_Google-Skywater-130nm/blob/main/README.md#day-2--pll-labs-and-post-layout-simulations_1-pll-components-circuit-design_lec-9)

[1.	PLL components circuit design](https://github.com/ravi18171M/Phase-Locked-Loop_PLL_IC-design_on_Open-Source_Google-Skywater-130nm/blob/main/README.md#day-2--pll-labs-and-post-layout-simulations_1-pll-components-circuit-design_lec-9)

[2.	PLL components circuit simulations](https://github.com/ravi18171M/Phase-Locked-Loop_PLL_IC-design_on_Open-Source_Google-Skywater-130nm/blob/main/README.md#day2_2-pll-components-circuit-simulations_lec-10)

[3.	Steps to combine PLL sub-circuits and PLL full design simulation](https://github.com/ravi18171M/Phase-Locked-Loop_PLL_IC-design_on_Open-Source_Google-Skywater-130nm/blob/main/README.md#day2_3-steps-to-combine-pll-sub-circuits-and-pll-full-design-simulation_lec-11)

[4.	Troubleshooting steps](https://github.com/ravi18171M/Phase-Locked-Loop_PLL_IC-design_on_Open-Source_Google-Skywater-130nm/blob/main/README.md#day2_4-troubleshooting-steps_lec-12)

[5.	Layout design](https://github.com/ravi18171M/Phase-Locked-Loop_PLL_IC-design_on_Open-Source_Google-Skywater-130nm/blob/main/README.md#day2_5-layout-design_lec-13)

[6.	Layout Walkthrough](https://github.com/ravi18171M/Phase-Locked-Loop_PLL_IC-design_on_Open-Source_Google-Skywater-130nm/blob/main/README.md#day2_6-layout-walkthrough_lec-14)

[7.	Parasitics extraction](https://github.com/ravi18171M/Phase-Locked-Loop_PLL_IC-design_on_Open-Source_Google-Skywater-130nm/blob/main/README.md#day2_7-parasitics-extraction_lec-15)

[8.	Post Layout simulations](https://github.com/ravi18171M/Phase-Locked-Loop_PLL_IC-design_on_Open-Source_Google-Skywater-130nm/blob/main/README.md#day2_8-post-layout-simulations_lec-16)

[9.	Steps to combine layouts](https://github.com/ravi18171M/Phase-Locked-Loop_PLL_IC-design_on_Open-Source_Google-Skywater-130nm/blob/main/README.md#day2_9-steps-to-combine-layouts_lec--17)

[10. Tapeout theory](https://github.com/ravi18171M/Phase-Locked-Loop_PLL_IC-design_on_Open-Source_Google-Skywater-130nm/blob/main/README.md#day2_10-tapeout-theory_lec-18)

[11. Tapeout labs](https://github.com/ravi18171M/Phase-Locked-Loop_PLL_IC-design_on_Open-Source_Google-Skywater-130nm/blob/main/README.md#day2_11-tapeout-labs_lec-19)




[Reference](https://github.com/ravi18171M/Phase-Locked-Loop_PLL_IC-design_on_Open-Source_Google-Skywater-130nm/blob/main/README.md#reference-)


[Commands used](https://github.com/ravi18171M/Phase-Locked-Loop_PLL_IC-design_on_Open-Source_Google-Skywater-130nm/blob/main/README.md#commands-used)




===============================================================================

## Day 1 – PLL Theory and Lab setup_1. Introduction to PLL_Lec 1 

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

## Day1_2. Introduction to Phase Frequency Detector_Lec 2

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

## Day1_3. Introduction to Charge Pump_Lec 3

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

## Day1_4. Introduction to VCO and Frequency Divider_Lec 4

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

## Day1_5. Tool setup and design flow_Lec 5

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

## Day1_6. Introduction to PDK, specifications and pre-layout circuits_Lec 6

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

## Day1_7. Circuit design simulation tool - Ngspice Setup_Lec 7

1. Need 4 files to simulate included in sky130.lib:

                                            1. sky130_fd_pr__pfet_01v8__tt.pm3.spice
                                            3. sky130_fd_pr__nfet_01v8__tt.pm3.spice
                                            4. lod.spice
                                            5. invariant.spice
2. These files are in spice_lib folder from there path is to copied in sky130.lib.
3. Reference: avsdpll_1v8 (path is in reference)
4. pdk: google/skywater-pdk -> sky130_fd_pr

===============================================================================

## Day1_8. Layout design tool - Magic Setup_Lec 8

Tech used: sky130A.tech 

It is included in the work directory.

===============================================================================

## Day 2 – PLL Labs and post-layout simulations_1. PLL components circuit design_Lec 9
 
1. Invoke ngspice where .cir is present.
2. limits:
                
                node = 130nm but limit is 150nm
                Nmos Wmin = 360nm
                Pmos Wmin = 420nm

3. .cir is circuit file
4. 1st line is comment , .ic for initial condition, .include to include file 
5. user made lib = sky130.lib where model files are present eg sky130_fd_pr__pfet_01v8__tt.pm3.spice
6 Designing:

![image](https://user-images.githubusercontent.com/88277263/127839792-f94e53c7-0b7b-4883-8e09-dd48b3b15f0c.png)

![image](https://user-images.githubusercontent.com/88277263/127839824-c93407de-3a0c-46a3-8535-d6fe91ce3adb.png)
![image](https://user-images.githubusercontent.com/88277263/127839951-cc79da31-c786-41d7-94b1-7eeee5d92cc8.png)


===============================================================================

## Day2_2. PLL components circuit simulations_Lec 10

1. PFD:

![image](https://user-images.githubusercontent.com/88277263/127840613-4b0746ee-8654-4fff-af1f-19564542cd31.png)

![image](https://user-images.githubusercontent.com/88277263/127840661-e2c55e17-eb74-4d2d-adb0-da3a81c66167.png)

![image](https://user-images.githubusercontent.com/88277263/127840688-03fc16ae-6715-46a9-bc59-a237bc429d5a.png)

![image](https://user-images.githubusercontent.com/88277263/127840726-f494da37-b1b4-45b1-aa61-2054f50b66e3.png)

It’s a positive edge trigger

![image](https://user-images.githubusercontent.com/88277263/127840782-b1b89d68-f241-4fc7-847c-06731d0f3fc8.png)





2. Charge Pump:

![image](https://user-images.githubusercontent.com/88277263/127841845-b00e9200-7043-44b5-935e-072d5dd8e2df.png)

To avoid leakage that vary the vctrl for vco , extra stage at up and down.



A. For both up = down = 0

![image](https://user-images.githubusercontent.com/88277263/127841989-153d1f24-09e0-415d-bbdb-f9b8fd8dd4ea.png)

![image](https://user-images.githubusercontent.com/88277263/127842028-3a646252-9d05-4271-90e1-d136ec613698.png)

![image](https://user-images.githubusercontent.com/88277263/127842859-8fb69bb8-6ced-41e0-a37f-5af13c1809f5.png)




B. For pulse given at up signal 

![image](https://user-images.githubusercontent.com/88277263/127842266-51316d49-230e-4444-b92d-a758eac09b1c.png)

![image](https://user-images.githubusercontent.com/88277263/127842319-880961a4-e203-4e01-8a6c-b387591607c4.png)









3. VCO: 

![image](https://user-images.githubusercontent.com/88277263/127843132-8f3a2637-ee9d-4539-9103-7382e24e247c.png)

![image](https://user-images.githubusercontent.com/88277263/127843158-d6f728c8-4445-4e1d-a45a-ecb494d63750.png)

Extra inv at output for full swing 

![image](https://user-images.githubusercontent.com/88277263/127843189-59b06579-5739-4f42-a109-4a42e9041de6.png)

![image](https://user-images.githubusercontent.com/88277263/127843213-ee41a42c-bbed-4b07-ae34-7e81d21768e1.png)




4 Freq Division:

![image](https://user-images.githubusercontent.com/88277263/127843515-1131cd98-7423-4b08-80d8-22f62e972b97.png)

![image](https://user-images.githubusercontent.com/88277263/127843537-885715bc-3dce-46cb-874b-2a7ce71f3b24.png)

![image](https://user-images.githubusercontent.com/88277263/127843550-509f351b-ab11-4924-a2b3-2074c0d11cda.png)

![image](https://user-images.githubusercontent.com/88277263/127843561-9f744288-987c-40cf-bd3f-aaf9522e05fd.png)


===============================================================================

## Day2_3. Steps to combine PLL sub-circuits and PLL full design simulation_Lec 11

![image](https://user-images.githubusercontent.com/88277263/127843953-80128384-e53f-4464-b22e-8791807c8b5d.png)
![image](https://user-images.githubusercontent.com/88277263/127843975-06a07c24-f286-4e8d-88ef-250f638a267e.png)
![image](https://user-images.githubusercontent.com/88277263/127844000-5e3295e5-1877-4ef2-bf6c-2f8bd7c65af6.png)
![image](https://user-images.githubusercontent.com/88277263/127844018-54fdbf2a-49eb-4ab7-a733-b36b5e0f93d2.png)
![image](https://user-images.githubusercontent.com/88277263/127844038-ea27a447-60a8-425c-9619-bebae359a23c.png)
![image](https://user-images.githubusercontent.com/88277263/127844060-745685bd-842d-4e87-9a86-808c617790c1.png)

![image](https://user-images.githubusercontent.com/88277263/127844114-48158aad-1b01-4570-90b9-7c12a32844af.png)

![image](https://user-images.githubusercontent.com/88277263/127844132-9cd7e07d-d104-4051-9e02-4ddc1533f6c3.png)

===============================================================================

## Day2_4. Troubleshooting steps_Lec 12

1. if waveform is 1 or 0 constant we need to check connectivity, naming , parameters etc

2. If output is not multipier of input we need to verify freq range of VCO for our case it is 40- 100 Mhz.

3. there is limitation of PFD wrt phase difference is can detect hence there will be some phase difference remains even after locking . phase noise is measure of phase difference.

4. charge pump tcharge and tdischarge optimized.

5. loop filter sizing.

===============================================================================

## Day2_5. Layout design_Lec 13

1. Tech used : sky130A.tech

2. Need to have n-well in which p diffusion is made to make pmos

3. Check DRC

4. Parasitic extrc are available on pins only.

===============================================================================

## Day2_6. Layout Walkthrough_Lec 14

1. PFD: 

![image](https://user-images.githubusercontent.com/88277263/127845503-a7b0a05e-a562-4e80-b91c-a18f3d93759a.png)

Extra inverter at top and bottom in layout added wrt cicuit seen before.

![image](https://user-images.githubusercontent.com/88277263/127845525-f9edead4-013b-43ce-ab3e-f881847084b6.png)

2. Charge Pump: 

![image](https://user-images.githubusercontent.com/88277263/127845571-f6084676-90b5-4295-898c-8861902feef3.png)

![image](https://user-images.githubusercontent.com/88277263/127845588-1367dd1b-f030-46a6-9662-19a5f89dc231.png)

3 VCO:

![image](https://user-images.githubusercontent.com/88277263/127845668-b5396b25-ded8-49a4-9e55-2e0d87ec26f3.png)

A. 7 inverters are placed in layout to decrease the range of frequency.

B. Large output inverter for driving strength of VCO (current).

C. Additional inverter to provide full swing at the output.

![image](https://user-images.githubusercontent.com/88277263/127845733-e6a9ebc0-6df9-4605-8ee5-dc8045afaf4c.png)

4 FD: 

![image](https://user-images.githubusercontent.com/88277263/127845761-027b5ce4-80f2-4665-901a-875c098604ef.png)

![image](https://user-images.githubusercontent.com/88277263/127845773-f01278c8-9ca9-4f48-9da1-d9fea32b9987.png)

5 Mux:

![image](https://user-images.githubusercontent.com/88277263/127845800-61633fcd-c07f-4383-a487-d9c83896b634.png)

![image](https://user-images.githubusercontent.com/88277263/127845814-309e130a-9ed2-436d-9556-0c27e473775c.png)

cmd used:

![image](https://user-images.githubusercontent.com/88277263/127845859-236f22f3-1a93-448a-948c-50e85f62794c.png)

===============================================================================

## Day2_7. Parasitics extraction_Lec 15

1. PFD parasitic extrc

Open layout, after that select all using ‘i’ and then use following command.

![image](https://user-images.githubusercontent.com/88277263/127846279-458fde92-6d2f-4d74-8ce3-c8673c9f13b9.png)

Created PFD.spice, which has all parasitic C0 to C46 .

![image](https://user-images.githubusercontent.com/88277263/127846317-ab55c481-6e62-4b7a-89c6-32d98d18e1bf.png)
![image](https://user-images.githubusercontent.com/88277263/127846332-7799a3a8-5307-4412-b20d-8d9fccbac8ec.png)

Terms: ad = area of drain, pd = perimeter of drain. Need to make correct scale at the top

2. Charge pump extrc

![image](https://user-images.githubusercontent.com/88277263/127846401-3687e925-f935-4e79-8352-252c11aaf478.png)

![image](https://user-images.githubusercontent.com/88277263/127846419-8257c221-a385-4a86-b2b4-23995d85b313.png)

![image](https://user-images.githubusercontent.com/88277263/127846452-8f37ea2f-040c-4304-9e63-8322d5ae4fb8.png)
![image](https://user-images.githubusercontent.com/88277263/127846466-1bfeb200-4ba9-4de2-b25a-1860a0d65425.png)

3. VCO parastitic extrc

![image](https://user-images.githubusercontent.com/88277263/127846530-6621db4f-6822-4622-aca5-0099a403ad49.png)

![image](https://user-images.githubusercontent.com/88277263/127846549-6371eb63-2b1c-4ce2-aa79-029d970c4379.png)

![image](https://user-images.githubusercontent.com/88277263/127846567-012ba2b9-1306-4998-be45-c26aaafa3b1c.png)
![image](https://user-images.githubusercontent.com/88277263/127846583-ad22d58b-7739-42bd-8f2e-986b378a22ac.png)

4. Freq Div parasitic extrc

![image](https://user-images.githubusercontent.com/88277263/127846655-e6cff06e-6ba4-4d9a-bdbd-b9ef87fd3122.png)

![image](https://user-images.githubusercontent.com/88277263/127846671-a993042c-1510-4e7b-b292-1ab101f47895.png)

![image](https://user-images.githubusercontent.com/88277263/127846680-f5bc7799-58bc-4a35-a396-d4eee6d71b6c.png)

![image](https://user-images.githubusercontent.com/88277263/127846692-9931c6b4-84da-445b-9a00-bde6fa397bb5.png)

===============================================================================

## Day2_8. Post Layout simulations_Lec 16

For post layout sim we create file which includes lib and extrc .spice content and required stimuli.

1. PFD post layout sim

![image](https://user-images.githubusercontent.com/88277263/127847225-1ba199b2-a47e-402d-a251-09eed20ff2c0.png)
![image](https://user-images.githubusercontent.com/88277263/127847234-175385fd-84a8-4b6d-87fb-614f28933cf9.png)

![image](https://user-images.githubusercontent.com/88277263/127847245-699de60c-8776-4a29-bdff-e166b52a93d2.png)

![image](https://user-images.githubusercontent.com/88277263/127847264-d05b1c33-8d8e-4524-a940-502292388c5d.png)

![image](https://user-images.githubusercontent.com/88277263/127847281-1b62ace6-00fb-4da4-b79e-895a579297cb.png)

2 Charge Pump post layout sim

![image](https://user-images.githubusercontent.com/88277263/127847387-ae4550d7-d120-4ee5-825d-9e02de4d6819.png)
![image](https://user-images.githubusercontent.com/88277263/127847402-2a3f12e5-a74e-4d4c-96fc-79ca3aebd951.png)

![image](https://user-images.githubusercontent.com/88277263/127847422-2b5b6b07-6b53-4a39-9f31-40c3a254291a.png)

3 VCO post layout sim

![image](https://user-images.githubusercontent.com/88277263/127847481-48afa7b1-54cc-4cef-854f-ba96749bfc94.png)
![image](https://user-images.githubusercontent.com/88277263/127847492-ecd2fdea-dd51-44f7-94bb-a4e518168483.png)

![image](https://user-images.githubusercontent.com/88277263/127847539-47f69e9b-282c-47c7-9472-79d16b73be53.png)

4 Freq Div post layout sim

![image](https://user-images.githubusercontent.com/88277263/127847582-e1cd64a3-66e1-4609-9945-90f5e07b7830.png)
![image](https://user-images.githubusercontent.com/88277263/127847599-4e9a3397-b529-49e7-9a43-8bda7d61e8d7.png)

![image](https://user-images.githubusercontent.com/88277263/127847617-33f1b7ef-0249-4488-b9bd-742d5b4d8931.png)

===============================================================================

## Day2_9. Steps to combine layouts_Lec – 17

1. To open magic:

magic –T  sky130A.tech

cell -> place instance 
                                                        
                                                        I = to select layout
                                                        X = to open layout
                                                        m = to move
                                                        space = for wire 
                                                        rt clk = to cancel wire select
                                                        three time space = to get in normal from wire mode 
2. MUX is used to control input of VCO via Charge pump or External control.
3. No loop filter is used in PLL we have used.
4. file -> write GDS     for converting layout to GDS format for FAB.

Extraction of PLL Layout:

![image](https://user-images.githubusercontent.com/88277263/127848691-f63f2101-7498-4d05-b071-d64df060af34.png)

![image](https://user-images.githubusercontent.com/88277263/127848719-3487db46-2412-4c61-bbaf-1b802b072200.png)

![image](https://user-images.githubusercontent.com/88277263/127848739-1609fa3a-7666-4518-925a-c3f17be34775.png)

Extracted PLL spice: 

![image](https://user-images.githubusercontent.com/88277263/127848813-9f492379-c87e-4b57-8359-1210e422f4ec.png)

![image](https://user-images.githubusercontent.com/88277263/127848835-ee403d07-c547-4b3f-8393-6107dcfd34cb.png)

![image](https://user-images.githubusercontent.com/88277263/127848857-0f75a56b-945e-4fc6-b3fb-2bafc6fe631f.png)

Making .cir for post layout sim:

![image](https://user-images.githubusercontent.com/88277263/127848951-1d42bda6-56db-4300-984a-91d4dd2ec4d6.png)
![image](https://user-images.githubusercontent.com/88277263/127848967-7d7d04bc-0666-4552-aec6-d04a90d1f117.png)
![image](https://user-images.githubusercontent.com/88277263/127848975-b3a8db07-883e-479c-b4bd-384b4c47f382.png)
![image](https://user-images.githubusercontent.com/88277263/127848992-52fcfe83-7421-42e9-aac2-2eaa8c15324b.png)
![image](https://user-images.githubusercontent.com/88277263/127849013-14b5dd08-3a38-46c9-82d2-6dc742aa9b18.png)

Simulating Post layout PLL 

![image](https://user-images.githubusercontent.com/88277263/127849094-b5c44a7b-c3c0-4c13-bfc5-949acd19e9d4.png)

![image](https://user-images.githubusercontent.com/88277263/127849114-6c8691ad-68cd-471f-a729-bc3cf4bdabb9.png)

![image](https://user-images.githubusercontent.com/88277263/127849159-acef71f0-eebc-4fea-807f-41ae91e629ea.png)

![image](https://user-images.githubusercontent.com/88277263/127849181-75eaa3eb-c58e-41ea-a9e5-15925ad4f50d.png)

![image](https://user-images.githubusercontent.com/88277263/127849194-474990cb-3d39-49cb-a1d7-173dd06239a0.png)

===============================================================================

## Day2_10. Tapeout theory_Lec 18

1. Tapeout is sending design to fab , after preparing it.

Preparing means: adding io pads, peripherals, memory units, testing mech etc. along with main IP.

2. For complete functioning of IP we need SOC which is provided by efabless named as caravel. It has user project area where we add our IP to make it working. We don’t need to care about things except the pins.

![image](https://user-images.githubusercontent.com/88277263/127849605-31763160-8b80-4228-b15a-7a558bf836b2.png)

===============================================================================

## Day2_11. Tapeout labs_lec 19

1. leared about placement of our design in User Praject Area of Caravel available at efabless github repository.
2. We will download user_analog_project_wrapper_emplty.gds.gz and extract it and later place our design in the empty layout space available with fixed pin provided.
3. We are having separate pins for analog, digital, pwr supply, io pins etc.
4. steps : 
                                                    
                                                    1. https://github.com/efabless
                                                    2. caravel_user_project_analog
                                                    3. caravel @ 13f2590
                                                    4. gds
                                                    5. user_analog_project_wrapper_empty.gds.gz
                                                    6. download copy code to work directory
                                                    7. gzip -d user_project_wrapper_empty.gds.gz
                  
![image](https://user-images.githubusercontent.com/88277263/127850288-1f943c93-1902-4e45-9700-2556e68713e0.png)

![image](https://user-images.githubusercontent.com/88277263/127850303-c0886627-3348-4c05-a80a-d13102616c34.png)

It is empty, we place our design inside it and connect pins to port available.

io_analog[0] is in metal 3 layer, so need contact to connect with PLL pins .

Our PLL has 5 pins en for CP&VCO, ref_clk, out_clk and vco_direct_inp. Except vco_direct_inp all are need io pins. VCCD, VSSD used for power supply.

===============================================================================

## Commands used:

                                      nano <file.cir> 			             // to edit file
                                      ngspice < file.cir> 		            // to invoke ngspice
                                      git clone <path>  			        // to create copy of github repo
                                      magic –T < .tech file> <.mag file> 	// to invoke magic with given layout
                                      ls 					                // list of files present at that location
                                      clear 					            // clear screan
                                      exit  					            // exit from ngspice 
                                      touch <file name>  			        // to create file


===============================================================================

## Work Directory:

![image](https://user-images.githubusercontent.com/88277263/127850855-d1fdd1d5-efbb-412d-9e3c-219079e9280e.png)

===============================================================================

## Reference :  

https://github.com/lakshmi-sathi/avsdpll_1v8.git

===============================================================================
            
## Acknowledgements:

1. Thank you!! Kunal Ghosh, Co-founder, VSD Corp. Pvt. Ltd. - kunalghosh@gmail.com for providing this Workshop.

2. Thank you!! Lakshmi S, MS ECE - lakshmi.sathi96@gmail.com for helping and providing resources during the Workshop.

===============================================================================

Thank you !!

Ravi Kumar Gupta 
gravikumargupta@gmail.com

===============================================================================




