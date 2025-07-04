
## 2230 USB4 SSD Enclosure Design


The purpose of this project is to verify the feasibility of a 40Gbps SSD enclosure solution in limited volume. 

This design has gone through several iterations. The current open source design file includes support for active cooling and has considerable compatibility.

The finished product of the open-source file is shown in the picture. The design of the adaptive shell is still in the planning stage.

![image](https://github.com/Leaves232/2230-USB4-SSD-Enclosure-Design/blob/main/USB4%202230%20Enclosure%20Images/QQ%E5%9B%BE%E7%89%87202506080921849.jpg)
![image](https://github.com/Leaves232/2230-USB4-SSD-Enclosure-Design/blob/main/USB4%202230%20Enclosure%20Images/QQ%E5%9B%BE%E7%89%8720250608104204.jpg)


### Function Availability

Speed ​​tests using a P44 Pro 2T also confirmed that the design is fully functional

![image](https://github.com/Leaves232/2230-USB4-SSD-Enclosure-Design/blob/main/USB4%202230%20Enclosure%20Images/QQ%E5%9B%BE%E7%89%8720250608104810.png)


This design has been checked to widely compatible with SSD.

It should be noted that due to limitation of the 3.3V Buck, it cannot meet the power consumption requirements of 4T SSDs. **Please use it with SSDs within 2T**.



## HOW TO USE FILES



**ASM2464PD DEMO Board B2 [Altium Designer]** folder contains the design source files developed using Altium Designer. You can make secondary modifications based on these files. The others are files used for finished product manufacturing.


### PCB Manufacturing


**Fabrication Files For DEMO Board B2** contains complete Gerber and drilling files for PCB production, which can be compressed and uploaded directly to board manufacturers such as JLC and Huaqiu for production. 

The PCB in Image Sets was made by Huaqiu PCB, and the stackup used was **04161H02-1080**. If you plan to produce the same PCB, please sent it directly to Huaqiu according to the corresponding parameters. 

If you plan to produce via other manufacturers, please emphasize to the production staff that the differential line impedance of the top and bottom layers should be controlled to about 85ohm according to the impedance requirements in the folder.

| 参数/Configuration    | 下单参数/Parameter|
| --------------------- | --------------------- |
|板材类型/Board Material Type      | FR-4      |
| 板子层数/Number of Layers   | 4        |
| 板子厚度/Board Thickness   | 1.6      |
| 最小线宽线距/Minimum Trace Width/Space   | 3.5 / 3.5 mil        |
| 最小过孔/Minimum Via Size   | 0.20 mm        |
| BGA   | 无/None      |
| 半孔/Castellated Hole   | 无需/Not required        |
| 包边/Edge Bonding / Board Edge Plating   | 无需/Not required        |
| 盲埋孔/Buried Via  | 无/None       |
| 阻抗/Impedance Control  | 有/Require        |
| 叠层结构/Layer Stack-up Structure   | 04161H02-1080       |
| 焊盘喷镀/Surface Finish   | 沉金(1u)/ENIG (1μm Au)       |
| 外层铜厚/Outer Layer Copper Weight   | 1oz        |
| 内层铜厚/Inner Layer Copper Weight   | 0.5oz      |
| 阻焊颜色/Solder Mask Color   | 蓝色/Blue       |
| 字符颜色/Legend Color   | 白色/White       |
| 阻焊覆盖/Solder Mask Coverage  | 过孔盖油/Via Tent       |
| 盘中孔/Via-in-Pad  | 无/None        |
| 沉金厚度/Electroless Nickel Immersion Gold  | 1 μ″        |
| 板材品牌/Laminate Brand   | 建滔        |
| TG值/Tg Value (Glass Transition Temperature)   | TG150        |



### SMT Manufacturing


**Bill of Materials for B2 Sample.xlsx** could be used to prepare components for PCBA manufacturing.

**Pick Place for ASM2464PD - B2 Sample.csv** is the location coordinates of each component, which is used to provide parameters for the SMT placement machine.

 When purchasing materials on your own, Please pay attention to packaging, capacitor withstand voltage, and price issues, or refer to the material selection list I used at Huaqiu **PCBA Project - BOM Quotation for 2230 USB4 Enclosure**

Please refer to the picture for SMT finished product effect

![image](https://github.com/Leaves232/2230-USB4-SSD-Enclosure-Design/blob/main/USB4%202230%20Enclosure%20Images/QQ%E5%9B%BE%E7%89%8720250607163928.jpg)



### Firmware Write


It is recommended to connect the completed ASM2464PD board to the USB port of computer when you try to write the firmware.

Download **ASM2464PD_FW_250123_85_00_00.zip** and unzip it to a separate folder

Unzip **20231221_ASM246xMPTool_v1.0.4.1** and run **ASM246xMPTool.exe**

Please follow the prompts below

![image](https://github.com/Leaves232/2230-USB4-SSD-Enclosure-Design/blob/main/USB4%202230%20Enclosure%20Images/v2-363b0b96c0792ce4a40c8168746c58be_1440w.png)

For other tips, please refer to the ASM2464PD_PDX mptool instructions in the folder


### Cooling Fan

Caution: ASM2464PD finished product will inevitably overheat and disconnect without heat dissipation.

The cooling fan in the demo is obtained by cutting the cooling module of Lenovo Legion Pro2.

You can connect it with flying wires, apply silicone grease and press it directly on the 2464 main controller.






### Congratulations, after completing the above steps you have a fully functional USB4 2230 SSD enclosure !




## License

The design is jointly completed by **@Leaves** and **@七上八下**. 

This project is open sourced under the MIT protocol.

