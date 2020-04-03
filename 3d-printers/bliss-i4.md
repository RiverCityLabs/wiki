# Bliss - i4

## Useful Links

needs a link to Octoprint

## How to Print

Please refer to the [How to Print](how-to-print.md) guide for detailed instructions

## Slicer Setup

1. Open Cura LE
2. Go to Settings &gt; Printers &gt; Add printer
3. Click Other \(see figure 1\)
4. Click "Custom" then "Custom FDM Printer" then click Add Printer \(see figure 2\)
5. Click Add Printer
6. Enter Machine Setting config noted below
   1. Follow the Green Boxes
   2. Printer Tab
      1. Configure Printer \(see figure 3.1\)
      2. Enter custom start Gcode \(see figure 3.2\)
      3. Enter custom end Gcode \(See figure 3.3\)
   3. Hot End Tab
      1. Configure Hotend \(see figure 4\)
7. Click Finish

![figure 1](../.gitbook/assets/image%20%2843%29.png)

![Figure 2](../.gitbook/assets/image%20%2853%29.png)

![Figure 3.1](../.gitbook/assets/image%20%2834%29.png)

Custom Start Gcode - Figure 3.2

```text
;This profile is designed specifically for RCLi4 3D Printer
;Basic slice data:
;Sliced at: {day} {date} {time}
;Layer height: {layer_height}
;Walls: {wall_thickness}
;Fill: {fill_density}
;Estimated Print time: {print_time}
;Filament used: {filament_amount}m {filament_weight}g
;Filament cost: {filament_cost}
G21
G90
M82
G92 E0                       ; set extruder position to 0
M140 S60                     ; get bed heated up
G0 Z15                       ; make sure nozzle is raised before homing
G28 X0Y0                     ; home X and Y
G1 X160 Y225 F1000           ; move to safe homing position above button
M109 R170                    ; soften filament for z homing
G28 Z0                       ; home Z
M104 S160                    ; wipe temp
G1 E-30 F100                 ; suck up 30mm of filament
G1 Z15                       ; move above button
G1 X125 Y223 F3000           ; move above wiper pad
G1 Z4.7                      ; push nozzle into wiper
G1 X120 Y224 F1000           ; slow wipe
G1 X115 Y224 F1000           ; slow wipe
G1 X110 Y224 F1000           ; slow wipe
G1 X115 Y221 F1000           ; slow wipe
G1 X105 Y224 F1000           ; slow wipe
G1 X120 Y221 F1000           ; slow wipe
G1 X100 Y224 F2000           ; fast wipe
G1 X90 Y221 F2000            ; fast wipe
G1 X95 Y224 F2000            ; fast wipe
G1 X85 Y221 F2000            ; fast wipe
G1 X80 Y224 F2000            ; fast wipe
G1 X75 Y221 F2000            ; fast wipe
G1 X65 Y224 F2000            ; fast wipe
G1 X70 Y221 F2000            ; fast wipe
G1 X60 Y224 F2000            ; fast wipe
G1 X65 Y221 F2000            ; fast wipe
G1 X95 Y224 F2000            ; fast wipe
G1 X55 Y221 Z5.7 F2000         ; fast wipe
G1 X60 Y224 F2000            ; fast wipe
G1 X50 Y222 F2000            ; fast wipe
G1 X55 Y221 F2000            ; fast wipe
G1 X50 Y222 Z5.2 F1000       ; slow wipe
G1 X48 Y224 F1000            ; slow wipe
G1 Z15                       ; raise extruder
M109 R160                    ; heat to probe temp
G1 X0 Y0                   ; move above probe
M204 S100                    ; set accel for probing
G29                          ; probe sequence (for auto-leveling)
M204 S500                    ; set accel back to normal
G0 Z15
G0 X260
G4 S1                        ; pause
M117 Heating...              ; LCD status message
M140 S{print_bed_temperature}; get bed heating up
M109 R{print_temperature}    ; set extruder temp and wait
M190 R{print_bed_temperature}; get bed temping up during first layer
G1 Z2 E0 F75                 ; extrude filament back into nozzle
M117 RCLi4 Printing...         ; LCD status message
```

Custom End Gcode - Figure 3.3

```text
;End GCode
M104 S0                     ;extruder heater off
M140 S0                     ;heated bed heater off (if you have it)
G91                                    ;relative positioning
G1 E-1 F300                            ;retract the filament a bit before lifting the nozzle, to release some of the pressure
G1 Z+0.5 E-5 X-20 Y-20 F{travel_speed} ;move Z up a bit and retract filament even more
G28 X0 Y0                              ;move X/Y to min endstops, so the head is out of the way
M84                         ;steppers off
G90                         ;absolute positioning
;{profile_string}
```

![Figure 4](../.gitbook/assets/image%20%285%29.png)

