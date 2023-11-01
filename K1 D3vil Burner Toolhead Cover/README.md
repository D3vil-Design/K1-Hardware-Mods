# D3D K1 D3vil Burner V3

**The long awaited D3vil Burner by the D3D team, featuring Knomi support, is here!**

<img style="width: 100%; height: 100%" width="100%" class="lazy" src="https://raw.githubusercontent.com/D3vil-Design/K1-Hardware-Mods/main/K1%20D3vil%20Burner%20Toolhead%20Cover/images/cover-1.jpg">

<img style="width: 100%; height: 100%" width="100%" class="lazy" src="https://raw.githubusercontent.com/D3vil-Design/K1-Hardware-Mods/main/K1%20D3vil%20Burner%20Toolhead%20Cover/images/cover-2.jpg">

<img style="width: 100%; height: 100%" width="100%" class="lazy" src="https://raw.githubusercontent.com/D3vil-Design/K1-Hardware-Mods/main/K1%20D3vil%20Burner%20Toolhead%20Cover/images/cover-3.jpg">

## Introduction

D3vil Design is proud to release the D3vil Burner toolhead cover for the Creality K1 for **free**. Packed with features, the team has worked meticulously to make sure that the cover is ready for release and as easy as a drop-in as possible with the limited space in the stock Creality K1 toolhead setup.

## Features

- Drop in replacement for the Creality K1 - no permenant modifications!
- Full Knomi support - view print progress real time, and add a little flair to your toolhead!
- Customizable LED featuring the D3vil Design logo - use any LED to match the style of your setup!
- Lightweight - 3.5 grams **LIGHTER** than the stock toolhead! (tests using ASA/ABS+, stock K1 shroud at 23.8 grams, D3vil Burner printed in ASA is 20.3 grams)

## Support

Join our [Discord](https://discord.gg/vPr5DjfHUJ) to chat with the team and find support for this product and anything else that D3D puts out :)

## Knomi 

for those who asked, you can purchase Knomi directly from the (non affiliate) link below 
https://biqu.equipment/collections/lcd/products/bigtreetech-knomi-v1-0


## Installation Guide

1. Download and print both STLs in this folder - the toolhead cover and the D3D logo. Recommended print settings for each are as follows:

   ##### D3vil Burner Toolhead Cover

   - Material: ABS, ASA, or another heat-resistant material
   - Layer Height: 0.2
   - Line width: 0.4
   - Walls: 3
   - Top/Bottom Layers: 3
   - Supports required (Top Z distance somewhere around 0.15)
   - orientation: print it facing up for the best results. 
   - Color: Your Choice!
     

   ##### D3vil Burner D3D Logo

   - Material: ABS, ASA, PETG, or another heat-resistant material
   - Layer Height: 0.2
   - Line width: 0.4
   - Walls: 3
   - Top/Bottom Layers: 3
   - Supports required (Top Z distance somewhere around 0.15)
   - Color: White or Transparent (we want light to shine through)

2. Remove the two screws from the stock toolhead cover and slide the cover off
3. Disconnect the front fan from the toolhead board and remove the fan from the stock toolhead cover
4. Slide the D3D Logo piece into the slot on the new toolhead's slot.
5. Connect a wire to the Knomi:

   ##### If you're not using an LED:

   5a. Find or create an MX1.25 (2pin) to MX1.25 (3pin) wire. Red to red, black to black according to the pinout shown on the board itself (Red to V and Black to G). We won't use the 3rd pin - this is just so we can connect it easily.

   5b. Connect the MX1.25 2pin to the Knomi **AND GENTLY PRY OFF THE USB PORT FROM THE KNOMI. IT DOES NOT FIT IN A STOCK SETUP**, then GENTLY (do not force, you'll crack the screen!) slide the Knomi into it's place from the back in.

   ##### If you are using an LED:

   <img style="width: 100%; height: 100%" width="100%" class="lazy" src="https://raw.githubusercontent.com/D3vil-Design/K1-Hardware-Mods/main/K1%20D3vil%20Burner%20Toolhead%20Cover/images/wiring-example-with-led.jpg">

   5a. Create a three-way wire. This wire should be an MX1.25 (2pin) to MX1.25 (3pin) to V/G (whatever your LED needs) wire. Red to red to read, black to black to black according to the pinout shown on the board itself (Red to V and Black to G). We won't use the 3rd pin - this is just so we can connect it easily.

    <img style="width: 100%; height: 100%" width="100%" class="lazy" src="https://raw.githubusercontent.com/D3vil-Design/K1-Hardware-Mods/main/K1%20D3vil%20Burner%20Toolhead%20Cover/images/db connector.jpg">

   5b. Solder or attach your V/G to your LED - the voltage is 5V coming from the toolboard - make sure your LED supports this or use a resistor.

   5c. There are two slots where you can lay your wires to prop up the LED. Attach those and prop your LED against the D3D logo piece.

   5d. Connect the MX1.25 2pin to the Knomi **AND GENTLY PRY OFF THE USB PORT FROM THE KNOMI. IT DOES NOT FIT IN A STOCK SETUP**, then GENTLY (do not force, you'll crack the screen!) slide the Knomi into it's place from the back in.

7. Slide the fan against the Knomi and attach the fan using the stock screws.
8. Connect the other end of the Knomi wire to the free filament sensor port on the toolhead board (again, outlined on the pinout shown on the board, Red to V and Black to G).
9. Re-attach the fan wire to the toolhead board.
10. Slide the D3vil Burner on to the toolhead and re-attach using the stock screws.
11. Voíla! Re-run input shaping, connect your Knomi following [BTT's instructions](https://github.com/bigtreetech/KNOMI/blob/master/KNOMI_USER_GUIDE.pdf).
12. NOTE: When connecting to Knomi Via wifi, in the setup screen, you will have to Add the IP address of your Printer ( Since this only works with Rooted Printers ) you will have to add the IP and the Port (ex: 192.168.1.10:4408 ).

And you're set!

If you would like to support the team to fund future projects, you can visit us at our [Patreon](https://www.patreon.com/D3vilDesign). We will begin posting behind the scenes projects, beta access to projects in flight, and more exclusively for our [Patreon](https://www.patreon.com/D3vilDesign) supporters.

-----------
If you wish to activate the Homing Macro please check the update below 

Thanks to .... 

For homing, if you put macro as it, it will throw an error 'G28 is called recursively'.
I have found that come from macro defined in sensorless.cfg

So to make it work, first add the macro at end of file
[gcode_macro G28]
rename_existing: G0028
variable_homing:False
gcode:
  RESPOND TYPE=command MSG='Custom G28 called'
  SET_GCODE_VARIABLE MACRO=G28 VARIABLE=homing VALUE=True
  G0028 {rawparams}
  SET_GCODE_VARIABLE MACRO=G28 VARIABLE=homing VALUE=False

atfer what find _HOME_X, _HOME_Y and _HOME_Z macro and replace G28 in it by G0028 like this
[gcode_macro _HOME_X]
gcode:
  _IF_MOVE_XY
  {% if printer['gcode_macro xyz_ready'].x_ready|int == 1 %}
    {% if (printer.configfile.settings['stepper_x'].position_max - printer.toolhead.position.x)|round < 10 %}
      {% set x_park = (10 - (printer.configfile.settings['stepper_x'].position_max - printer.toolhead.position.x))|round %}
      {% if x_park > 0 %}
        G91
       G1 x-{x_park} F3600
        G90
        G4 P1000
      {% endif %}
    {% endif %}
  {% endif %}
  
# SET_TMC_FIELD FIELD=SGTHRS STEPPER=stepper_y VALUE=70
# SET_TMC_FIELD FIELD=SGTHRS STEPPER=stepper_x VALUE=70
# Home
  RESPOND TYPE=command MSG='Call G28 in _HOME_X macro'
  G0028 X #<<====== HERE
  SET_GCODE_VARIABLE MACRO=xyz_ready VARIABLE=x_ready VALUE=1
# Move away
  G91
  G1 x-10 F3600
  G90
# Wait just a second (give StallGuard registers time to clear)
 G4 P2000

For bed leveling, as i'm using Kamp, in Adaptative_Meshing.cfg, BED_MESH_CALIBRATE Macro is already defined
So just add "variable_probing:False" after rename existing and SET_GCODE_VARIABLE before and after calling _BED_MESH_CALIBRATE

Here is the modified macro :
[gcode_macro BED_MESH_CALIBRATE]
rename_existing: _BED_MESH_CALIBRATE
variable_probing:False
gcode:

{% set all_points = printer.exclude_object.objects | map(attribute='polygon') | sum(start=[]) %}                                # Gather all object points
{% set bed_mesh_min = printer.configfile.settings.bed_mesh.mesh_min %}                                                          # Get bed mesh min from printer.cfg
{% set bed_mesh_max = printer.configfile.settings.bed_mesh.mesh_max %}                                                          # Get bed mesh max from printer.cfg
{% set probe_count = printer.configfile.settings.bed_mesh.probe_count %}                                                        # Get probe count from printer.cfg
{% set kamp_settings = printer["gcode_macro _KAMP_Settings"] %}                                                                 # Pull variables from _KAMP_Settings
{% set verbose_enable = kamp_settings.verbose_enable | abs %}                                                                   # Pull verbose setting from _KAMP_Settings
{% set probe_dock_enable = kamp_settings.probe_dock_enable | abs %}                                                             # Pull probe dockable probe settings from _KAMP_Settings
{% set attach_macro = kamp_settings.attach_macro | string %}                                                                    # Pull attach probe command from _KAMP_Settings
{% set detach_macro = kamp_settings.detach_macro | string %}                                                                    # Pull detach probe command from _KAMP_Settings
{% set mesh_margin = kamp_settings.mesh_margin | float %}                                                                       # Pull mesh margin setting from _KAMP_Settings
{% set fuzz_amount = kamp_settings.fuzz_amount | float %}                                                                       # Pull fuzz amount setting from _KAMP_Settings
{% set probe_count = probe_count if probe_count|length > 1 else probe_count * 2  %}                                             # If probe count is only a single number, convert it to 2. E.g. probe_count:7 = 7,7
{% set max_probe_point_distance_x = ( bed_mesh_max[0] - bed_mesh_min[0] ) / (probe_count[0] - 1)  %}                            # Determine max probe point distance
{% set max_probe_point_distance_y = ( bed_mesh_max[1] - bed_mesh_min[1] ) / (probe_count[1] - 1)  %}                            # Determine max probe point distance
{% set x_min = all_points | map(attribute=0) | min | default(bed_mesh_min[0]) %}                                                # Set x_min from smallest object x point
{% set y_min = all_points | map(attribute=1) | min | default(bed_mesh_min[1]) %}                                                # Set y_min from smallest object y point
{% set x_max = all_points | map(attribute=0) | max | default(bed_mesh_max[0]) %}                                                # Set x_max from largest object x point
{% set y_max = all_points | map(attribute=1) | max | default(bed_mesh_max[1]) %}                                                # Set y_max from largest object y point

{% set fuzz_range = range((0) | int, (fuzz_amount * 100) | int + 1) %}                                                          # Set fuzz_range between 0 and fuzz_amount
{% set adapted_x_min = x_min - mesh_margin - (fuzz_range | random / 100.0) %}                                                   # Adapt x_min to margin and fuzz constraints
{% set adapted_y_min = y_min - mesh_margin - (fuzz_range | random / 100.0) %}                                                   # Adapt y_min to margin and fuzz constraints
{% set adapted_x_max = x_max + mesh_margin + (fuzz_range | random / 100.0) %}                                                   # Adapt x_max to margin and fuzz constraints
{% set adapted_y_max = y_max + mesh_margin + (fuzz_range | random / 100.0) %}                                                   # Adapt y_max to margin and fuzz constraints

{% set adapted_x_min = [adapted_x_min , bed_mesh_min[0]] | max %}                                                               # Compare adjustments to defaults and choose max
{% set adapted_y_min = [adapted_y_min , bed_mesh_min[1]] | max %}                                                               # Compare adjustments to defaults and choose max
{% set adapted_x_max = [adapted_x_max , bed_mesh_max[0]] | min %}                                                               # Compare adjustments to defaults and choose min
{% set adapted_y_max = [adapted_y_max , bed_mesh_max[1]] | min %}                                                               # Compare adjustments to defaults and choose min

{% set points_x = (((adapted_x_max - adapted_x_min) / max_probe_point_distance_x) | round(method='ceil') | int) + 1 %}          # Define probe_count's x point count and round up
{% set points_y = (((adapted_y_max - adapted_y_min) / max_probe_point_distance_y) | round(method='ceil') | int) + 1 %}          # Define probe_count's y point count and round up

{% if (points_x > points_y) %}
    {% set points_y = points_x %}
{% endif %}

{% if (points_x < points_y) %}
    {% set points_x = points_y %}
{% endif %}

{% if (([points_x, points_y]|max) > 6) %}                                                                                       # 
    {% set algorithm = "bicubic" %}                                                                                             # 
    {% set min_points = 4 %}                                                                                                    # 
{% else %}                                                                                                                      # Calculate if algorithm should be bicubic or lagrange
    {% set algorithm = "lagrange" %}                                                                                            # 
    {% set min_points = 3 %}                                                                                                    # 
{% endif %}                                                                                                                     # 

{% set points_x = [points_x , min_points]|max %}                                                                                # Set probe_count's x points to fit the calculated algorithm
{% set points_y = [points_y , min_points]|max %}                                                                                # Set probe_count's y points to fit the calculated algorithm
{% set points_x = [points_x , probe_count[0]]|min %}
{% set points_y = [points_y , probe_count[1]]|min %}

{% if verbose_enable == True %}                                                                                                 # If verbose is enabled, print information about KAMP's calculations
    {% if printer.exclude_object.objects != [] %}

        { action_respond_info( "Algorithm: {}.".format(                                                                              
            (algorithm),                                                                                                            
        )) }

        { action_respond_info("Default probe count: {},{}.".format(                                                                  
            (probe_count[0]),                                                                                                       
            (probe_count[1]),                                                                                                       
        )) }

        { action_respond_info("Adapted probe count: {},{}.".format(                                                                  
            (points_x),                                                                                                             
            (points_y),                                                                                                             
        )) }                                                                                                              

        {action_respond_info("Default mesh bounds: {}, {}.".format(                                                                  
            (bed_mesh_min[0],bed_mesh_min[1]),                                                                                      
            (bed_mesh_max[0],bed_mesh_max[1]),                                                                                      
        )) }

        {% if mesh_margin > 0 %}                                                                                                    
            {action_respond_info("Mesh margin is {}, mesh bounds extended by {}mm.".format(                                       
                (mesh_margin),                                                                                                      
                (mesh_margin),                                                                                       
            )) }                                                                                                                    
        {% else %}                                                                                                                  
            {action_respond_info("Mesh margin is 0, margin not increased.")}                                                        
        {% endif %}                                                                                                                 

        {% if fuzz_amount > 0 %}                                                                                                    
            {action_respond_info("Mesh point fuzzing enabled, points fuzzed up to {}mm.".format(                                     
                (fuzz_amount),                                                                                                      
            )) }                                                                                                                    
        {% else %}                                                                                                                  
            {action_respond_info("Fuzz amount is 0, mesh points not fuzzed.")}                                                      
        {% endif %}                                                                                                                 

        { action_respond_info("Adapted mesh bounds: {}, {}.".format(                                                                 
            (adapted_x_min, adapted_y_min),                                                                                         
            (adapted_x_max, adapted_y_max),                                                                                         
        )) }

        {action_respond_info("KAMP adjustments successful. Happy KAMPing!")}

    {% else %}

        {action_respond_info("No objects detected! Check your gcode and make sure that EXCLUDE_OBJECT_DEFINE is happening before BED_MESH_CALIBRATE is called. Defaulting to regular meshing.")}
        G4 P5000                                                                                                                # Wait 5 seconds to make error more visible
    {% endif %}

{% endif %}

{% if probe_dock_enable == True %}
    {attach_macro}                                                                                                              # Attach/deploy a probe if the probe is stored somewhere outside of the print area
{% endif %}

SET_GCODE_VARIABLE MACRO=BED_MESH_CALIBRATE VARIABLE=probing VALUE=True
_BED_MESH_CALIBRATE mesh_min={adapted_x_min},{adapted_y_min} mesh_max={adapted_x_max},{adapted_y_max} ALGORITHM={algorithm} PROBE_COUNT={points_x},{points_y}
SET_GCODE_VARIABLE MACRO=BED_MESH_CALIBRATE VARIABLE=probing VALUE=False

{% if probe_dock_enable == True %}
    {detach_macro}                                                                                                              # Detach/stow a probe if the probe is stored somewhere outside of the print area
{% endif %}                                                                                                                     # End of verbose
