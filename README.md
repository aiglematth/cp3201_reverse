# R65C22P2

## Config

### Auxiliary Control Register (ACR)
- Value set in init_env to 0x0c : ext clock, timer 2 time interrupt

### Peripheral Control Register (PCR)
- Value set in init_env to 0x00 : nothing to say

### Data Direction Register A (DDRA)
- Value set in init_env to 0xff : all lines are output

### Data Direction Register B (DDRB)
- Value set in init_env to 0xfd : all lines are output except PB1

### Output Register A (ORA)
- Value set in init_env to 0xff : all lines go high

### Output Register B (ORB)
- Value set in init_env to 0x04 : all lines go low except PB2

### Interrupt Enable Register
- Value set in init_env to 0xa0 : timer 2 interrupt is enabled

### Output Register A (ORA)
- Value set in init_env to 0xff : all lines go high

### Timer 2 
- Value set in init_env to 0x4c00 : 

# Serial ack = send 0 on line to ack

# [X00C01HU?] == get current port

# [XijC01GS?] with (ij = port) == 

# Command results

- `HU ij` -> set port (with ij = port)
- `ERijk` -> error ijk raised
- `VSijklm` -> something on sweep 
- `BLabcdefghijklmnop` -> set bandwith ab.cd ef.gh ij.kl mn.op
- `T1 ij` -> Temperature is ij degrees
- `B1 ij` -> i.j volts
- `P11` -> Main lo is locked
- `P1i` -> Main lo is unlocked
- `P1i` -> Main lo is sweeping **IS_IN_COMMAND_ID_MODE != 0**
- `ACijk` -> 
- `TIijkl` -> ijklm is the time in hours
- `ATij` -> ij attenuation in dB
- `AG` -> Automatic gain control 
- `AO` -> Automatic gain control 
- `GAijk` -> ijk AM video level
- `GFijk` -> ijk AM video level

# Command ID
- 0  : 
- 1  : Video if attenuation
- 2  : Continuous wave (CW) center frequency
- 3  : Start frequency
- 4  : Stop frequency
- 5  : 
- 6  :
- 7  :
- 8  :
- 9  : AM video level
- 10 : FM video level
- 11 : AGC state
- 12 : Temperature
- 13 : 
- 14 : Record ID bandwith
- 15 :
- 16 :
- 17 : Tuning resolution
- 18 : Sweep time
- 19 : 
- 20 : Step size
- 24 : Host baud rate
- 27 : Adjust viewing angle
- 28 : Adjust backlighting
- 32 : Deal with presets
- 36 : Enable or lock host
- 40 : GPIB address
- 41 : Unit address