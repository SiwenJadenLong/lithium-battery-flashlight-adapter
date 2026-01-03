---
# yaml-language-server: $schema=schemas\page.schema.json
Object type:
    - Page
Creation date: "2025-12-29T03:11:33Z"
Created by:
    - Siwen Long
Links:
    - Samsung 58E (CC5493F101) 5330mAh 10.7A Battery
    - Sinowatt 70HP 26650 7000mAh 14A Battery
id: bafyreic3wo3inzjztajtzenbvojdvyxrgd2omhgpq4noxvgmcx3pduz5ye
---
# Giant Flashlight Adapter   
Output 9v   
Average amperage draw, as measured with my multimeter, 320mA, it dropped from about 500mA over the course of 30secs.   
   
space expressed as cylinder:   
-104mm high   
-30.7mm dia   
   
Stated manufacturer specs:   
with 6 AA batteries in series for 9v,   
battery life of 2hrs.   
~~Assuming 2AH, that seems like an average draw of 1A~~ 1/3/26 way off compared to measurements   
   
[https://www.tractorsupply.com/tsc/product/surge-1-000-lumen-tactical-led-alkaline-flashlight-hhl3060as](https://www.tractorsupply.com/tsc/product/surge-1-000-lumen-tactical-led-alkaline-flashlight-hhl3060as)    
   
21700 Battery in interest:   
[Samsung 58E (CC5493F101) 5330mAh 10.7A Battery](https://www.18650batterystore.com/products/samsung-inr21700-58e-cc5493f101-5330mah-10-7a)    
26650 Battery in interest:   
[Sinowatt 70HP 26650 7000mAh 14A Battery](https://www.18650batterystore.com/products/sinowatt-70hp-26650-7000mah-14a-battery)    
Available components:   
- 3 gold plated Spring contacts   
   
   
PCB constrants:   
- Diameter of no more than 30mm   
- 2 Layer board   
- USB-C port needs to stick out enough for charging   
   
   
ICs of choice:   
- Battery charging: BQ2407   
    - Choose this because of low cost, low package complexity, 1.5A charging current   
- Battery protection: DW01A   
    - For preventing over discharging from the buck   
    - needs 2 N-Channel depletion mosfets   
- Voltage boast: MIC2295   
    - 1.2 Amp max, 74% efficiency at 1.2A, flashlight should pull about 1A. I'll need to test    
   
   
Battery life calculations:   
Battery: 7000mAh \| 4.2V   
Need to output: 9V 320mA/500mA (estimate/conservative)   
Efficiency of 74%   
   
Brain spill:   
- From negative terminal, I can run a wire to the pcb for ground   
- PCB can have spring terminal on bottom for space saving or I can run a wire   
- Haven't figured out how to maintain pressure to keep the springs touching. Thinking I can use the screws pressing of the end caps somehow, may be complicated. Oh wait →   
- I can have the negative cap need to be removed to insert the battery and then press the bottom cap against the battery using the screws that will go to the 3D printed housing   
- Will need a small donut hole in the pcb for wire of the positive end of the battery to the pcb.    
- Or I can coil up the wire and solder it only to the bottom of the pcb for more space. This would eliminate the potential issues of space on the pcb and I think I'd have the vertical space for it   
- Need to modify pcb, put holes in it for when I need to sandwich the plastic piece on top, not sure how to connect the 3D prints after I sandwich the pcb.   
   
   
   
