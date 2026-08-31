# ~~HandSTaMp~~ HandCHime

## Bill of Materials

| Reference | Silkscreen | Part                        | Footprint | Purpose                                        |
|-----------|------------|-----------------------------|-----------|------------------------------------------------|
| C1        | µ          | 4.7µF ceramic capacitor     | 0603      | Bulk decoupling capacitor for U1               |
| C2        | n          | 100nF ceramic capacitor     | 0603      | Decoupling capacitor for U1                    |
| D1        | D1         | PMEG2010EA Schottky diode   | SOD-323   | Reverse current protection                     |
| D2, D3    | D2, D3     | 2 × 1N4148 diodes           | SOD-123   | Matrix diodes for SW1/SW2                      |
| F1        | F          | 500mA fuse                  | 0603      | Current overload protection                    |
| J1        | J1         | HRO TYPE-C-31-M-12 USB port |           | For the pluggings in of USB cables             |
| R1, R2    | 1, 2       | 2 × 5.1kΩ resistors         | 0603      | USB power negotiation (Rd) resistors           |
| R3        | 3          | 5.1kΩ resistor              | 0603      | Boot circuit resistor                          |
| S1, S2    | *None*     | 2 × MX-compatible switches  | MX plate¹ | Keys for row 0, columns 0/1; mountings for PCB |
| S3        | *None*     | B3U-1000P                   |           | Boot switch                                    |
| U1        | *None*²    | CH32X035G8U6                | WQFN-28   | ~~Braaaains!~~ Microcontroller                 |
| U2        | U2         | PRTR5V0U2X                  | SOT-143   | ESD protection                                 |

##### Notes

 1. Three-pin “plate-mount” switches can be used as-is. To use five-pin “PCB-mount” switches,
    the two extra plastic alignment “pins” must be removed.
 2. U1 is positioned in the ~4×4mm area in the lower centre of the PCB.

## Debug Interface

The Serial Debug Interface (SDI) pins are assigned as follows:

 1. **S**quare Pin — **S**WDIO
 2. **C**ircular Pin — SW**C**LK

These pins are intended to be small enough to friction fit debug probe wires.
The pins can alternatively be used as the following extra GPIO pins:

 1. Square Pin — PC18
 2. Circular Pin — PC19

Note that these pins are underneath a switch and can only be soldered from the bottom.
Wires should be trimmed as close to the board as possible.
