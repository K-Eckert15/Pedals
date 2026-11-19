Bourns PTV111-3 vertical-shaft, M9x0.75 threaded-bushing potentiometer footprint
================================================================================

Source:
  https://www.bourns.com/data/global/pdfs/PTV111.pdf
  See PTV111-3 recommended PCB layout on the second page of the PDF.

Use for all three of these PTV111-3415A series variants, subject to verification:
  RV1: PTV111-3415A-B104 100k linear
  RV2: PTV111-3415A-B103 10k linear
  RV3: PTV111-3415A-A104 100k audio

FOOTPRINT GEOMETRY (all in millimetres):
  Pin 1 x=0.0, pin 2 x=2.5, pin 3 x=5.0, dummy pin x=7.5 at y=0
  Electrical pins have 1.0 mm plated drills, 1.8 mm outer copper pads.
  Dummy pin is solderable but unnumbered because not electrically connected.
  Two 2.0 x 2.1 mm non-plated mounting slots, separated 13.0 mm.
  Mounting slots are 11.0 mm from pin row.
  Pad 2 is the wiper. Pins 1 and 3 are the resistive ends.

INSTALL (from ~/Pedals/Distorter):
  unzip PTV111_KiCad_Footprint.zip -d .

KiCad > Preferences > Manage Footprint Libraries > Project Specific Libraries:
  Nickname: Distorter
  Library path: ${KIPRJMOD}/libraries/footprints/Distorter.pretty

Then assign to RV1, RV2 and RV3:
  Distorter:Potentiometer_Bourns_PTV111-3_VerticalShaft

STEP MODEL:
  This package does NOT contain the manufacturer STEP file.
  Copy your own PTV111 STEP file to libraries/3dmodels/, open Footprint
  Editor > Footprint Properties > 3D Models, add:
  ${KIPRJMOD}/libraries/3dmodels/<your_exact_step_filename>.step
  Adjust rotation/offset to match the physical shaft and terminal holes.

IMPORTANT BEFORE FABRICATION:
  This is a datasheet-based custom footprint, not an official manufacturer EDA model.
  Verify hole position and slot sizes against the latest drawing and by printing
  a 1:1 footprint or trial fitting a physical part. Check plated vs non-plated
  slot manufacturing support at your PCB fabricator and review the KiCad 3D view.
  Do not reuse this footprint for PTV111-1, -2 or -4 layouts.
