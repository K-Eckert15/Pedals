# SparkFun COM-15133 / Alpha SF17010F 3PDT stomp switch

This bundle is for the **Distorter** KiCad project located in `~/Pedals/Distorter`.

- **Part:** SparkFun COM-15133; DigiKey 1568-15133-ND
- **Function:** 3PDT latching (ON-ON), threaded M12 x 0.75 bushing, 9 PC-pin terminals.
- **Source mechanical drawing:** https://cdn.sparkfun.com/assets/3/a/9/c/4/DS-15133-Stomp_Switch.pdf
- **DigiKey:** https://www.digikey.com/en/products/detail/sparkfun-electronics/15133/9826562

## Install
From `~/Pedals/Distorter`, extract the archive directly into the project.
Register `libraries/symbols/COM-15133.kicad_sym` as a **project** symbol library named `COM-15133` (Schematic Editor -> Preferences -> Manage Symbol Libraries).
Register `libraries/footprints/Distorter.pretty` as a **project** footprint library named `Distorter` (PCB Editor -> Preferences -> Manage Footprint Libraries).

Add symbol `COM-15133:SW_3PDT_Stomp_COM-15133` to schematic, with footprint `Distorter:SW_3PDT_SparkFun_COM-15133`.

## Electrical pin numbering
The nine pads are numbered row-by-row, when viewing **the bottom of the switch / top of the PCB**, per the manufacturer's electrical schematic:

    1   2   3     pole A, common 2
    4   5   6     pole B, common 5
    7   8   9     pole C, common 8

Each center pin toggles between its two outside pins: 2<->1/3, 5<->4/6, 8<->7/9. The schematic symbol uses the same numbering. **Test contact behavior using a multimeter and physical part; verify orientation before fabrication.**

## PCB geometry
9 holes, drill diameter **1.2 mm**, centers **5.3 mm** apart horizontally and **4.8 mm** apart vertically (overall **10.6 x 9.6 mm**). Body outline approximately **19.6 x 17.0 mm**.

## 3D model accuracy
The bundled STEP model is **an approximate model drawn for this project**, not a manufacturer's certified STEP file. Body width/depth, pin pitch, and M12 bushing match the mechanical drawing at a first-order level. Its Z heights and fine details are approximated. Scale is **1.0**. Use it for early enclosure layout only, not for an interference-critical final assembly.

## Before ordering the PCB
1. Verify the nine pads and hole diameters against the exact purchased switch and page 2 of the Alpha PDF.
2. Confirm the model is correct side up: switch sits on PCB front, shaft points **away** from board.
3. Measure the panel-to-PCB distance; footswitch, pots, and jacks must all align with the enclosure.
4. Check in KiCad ERC and footprint association, and verify the position of each throw using a continuity meter.
