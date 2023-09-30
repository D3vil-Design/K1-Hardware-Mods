# D3D K1 D3vil Burner V3

**The long awaited D3vil Burner by the D3D team, featuring Knomi support, is here!**

<img style="width: 100%; height: 100%" width="100%" class="lazy" src="https://raw.githubusercontent.com/D3vil-Design/K1-Hardware-Mods/main/K1%20D3vil%20Burner%20Toolhead%20Cover/images/cover-1.jpg">

<img style="width: 100%; height: 100%" width="100%" class="lazy" src="https://raw.githubusercontent.com/D3vil-Design/K1-Hardware-Mods/main/K1%20D3vil%20Burner%20Toolhead%20Cover/images/cover-2.jpg">

<img style="width: 100%; height: 100%" width="100%" class="lazy" src="https://raw.githubusercontent.com/D3vil-Design/K1-Hardware-Mods/main/K1%20D3vil%20Burner%20Toolhead%20Cover/images/cover-3.jpg">

## Introduction

D3vil Design is proud to release the D3vil Burner toolhead cover for the Creality K1 for **free**. Packed with features, the team has worked meticulously to make sure that the cover is ready for release and as easy as a drop-in as possible with the limited space in the stock Creality K1 toolhead setup.

If you would like to support the team to fund future projects, you can visit us at our [Patreon](https://www.patreon.com/D3vilDesign). We will begin posting behind the scenes projects, beta access to projects in flight, and more exclusively for our [Patreon](https://www.patreon.com/D3vilDesign) supporters. If you're interested in more K1 work (and some "top secret" work outside of the K1 😉), please consider [supporting the team](https://www.patreon.com/D3vilDesign). All funds go directly to the development and support of the D3vil Design team!

## Features

- Drop in replacement for the Creality K1 - no permenant modifications!
- Full Knomi support - view print progress real time, and add a little flair to your toolhead!
- Customizable LED featuring the D3vil Design logo - use any LED to match the style of your setup!
- Lightweight - 3.5 grams **LIGHTER** than the stock toolhead! (tests using ASA/ABS+, stock K1 shroud at 23.8 grams, D3vil Burner printed in ASA is 20.3 grams)

## Installation Guide

1. Download and print both STLs in this folder - the toolhead cover and the D3D logo. Recommended print settings for each are as follows:

   ##### D3vil Burner Toolhead Cover

   - Material: ABS, ASA, or another heat-resistant material
   - Layer Height: 0.2
   - Line width: 0.4
   - Walls: 3
   - Top/Bottom Layers: 3
   - Supports required (Top Z distance somewhere around 0.15)
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

   5b. Solder or attach your V/G to your LED - the voltage is 5V coming from the toolboard - make sure your LED supports this or use a resistor.

   5c. There are two slots where you can lay your wires to prop up the LED. Attach those and prop your LED against the D3D logo piece.

   5d. Connect the MX1.25 2pin to the Knomi **AND GENTLY PRY OFF THE USB PORT FROM THE KNOMI. IT DOES NOT FIT IN A STOCK SETUP**, then GENTLY (do not force, you'll crack the screen!) slide the Knomi into it's place from the back in.

6. Slide the fan against the Knomi and attach the fan using the stock screws.
7. Connect the other end of the Knomi wire to the free filament sensor port on the toolhead board (again, outlined on the pinout shown on the board, Red to V and Black to G).
8. Re-attach the fan wire to the toolhead board.
9. Slide the D3vil Burner on to the toolhead and re-attach using the stock screws.
10. Voíla! Re-run input shaping, connect your Knomi following [BTT's instructions](https://github.com/bigtreetech/KNOMI/blob/master/KNOMI_USER_GUIDE.pdf), and you're set!
