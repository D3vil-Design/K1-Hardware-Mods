
<img style="width: 100%; height: 100%" width="100%" class="lazy" src="https://github.com/D3vil-Design/K1-Hardware-Mods/blob/main/K1%20FatBoys%20XY%20Joints/fatboys%20Images/Frame%2036%20(1).png?raw=true">

<img style="width: 100%; height: 100%" width="100%" class="lazy" src="https://github.com/D3vil-Design/K1-Hardware-Mods/blob/main/K1%20FatBoys%20XY%20Joints/fatboys%20Images/Untitled.png?raw=true">
<img style="width: 100%; height: 100%" width="100%" class="lazy" src="https://github.com/D3vil-Design/K1-Hardware-Mods/blob/main/K1%20FatBoys%20XY%20Joints/fatboys%20Images/Untitled%202.png?raw=true">
<img style="width: 100%; height: 100%" width="100%" class="lazy" src="https://github.com/D3vil-Design/K1-Hardware-Mods/blob/main/K1%20FatBoys%20XY%20Joints/fatboys%20Images/Untitled%203.png?raw=true">


Kindly if you dont know what you are doing , ask in our discord server: https://discord.gg/vPr5DjfHUJ

This joint are bigger by 5mm in both side which means it will reduce the overall X movment in the gantry on the K1 from 235 to 225 ( same build size ) 
- they can be used with the stock idlers ( if you are using the 8mm belt )
- or it can be used with any other 6mm idlers aswell.

Be advised to use the same M5x5mm grub screw to hold the rods in place instead of glue. (DO NOT OVERTIGHTEN)

changes might be needed to the printer.cfg file

For the K1:
change the [stepper_x] values below:
.
.
.
position_endstop: 226  ##stock value was 229
position_min: 0        ##stock value was -5
position_max: 226      ##stock value was 229

NOTE: the idea is to move you toolhead to X=10 and test move it from there 1mm at a time to see where the x carriage will touch the left XY joint.

For the K1 Max:

Needs to bee tested step by step ... will be updated



This will be updated soon™️

special thanks to all the ones who tested it and reported thier findings 


If you would like to support the team to fund future projects, you can visit us at our [Patreon](https://www.patreon.com/D3vilDesign).
