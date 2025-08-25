# 4x1 Multiplexer Using Only NOR Gates

## Introduction
This project is about building a 4x1 multiplexer using only 2-input NOR gates in Logisim Evolution. I wanted to try out how universal gates like NOR can be used to design something as common as a multiplexer without relying on other gates.

All the required logic (NOT, AND, OR) was derived from NOR gate operations, and the full multiplexer was then put together step by step.

## Objective
The goal was to design a fully working 4x1 multiplexer with only NOR gates, test it with different input combinations, and make sure the output matches the expected behavior.

## Theory
A 4x1 multiplexer selects one of four inputs (I0, I1, I2, I3) based on two select lines (S1, S0). The output can be written as:


To implement this using only NOR gates:
- NOT A = A NOR A
- A AND B = (A' NOR B')'
- A OR B = (A NOR B) NOR (A NOR B)

## Circuit Design
The design uses:
- 17 two-input NOR gates
- 6 input pins (I0–I3, S0, S1)
- 1 output pin (Y)

I uploaded all circuit files in the folder `Circuit Files` and all simulation screenshots in the folder `Images`.

### Main Circuit
Here’s the complete design in Logisim Evolution:
<img width="1920" height="1080" alt="Main Circuit" src="https://github.com/user-attachments/assets/4864862c-9e36-4be4-bb90-b3a8f0a843de" />


### Working
1. Inputs and select lines are set using switches.
2. The select lines are inverted using NOR gates to get S0' and S1'.
3. Four product terms (P1–P4) are built using combinations of inputs and select lines.
4. Finally, these product terms are combined using NOR-based OR logic to get the output Y.

## Testing
I tested the multiplexer with different select lines and inputs. The output always matched the expected result.

### Test Case 1
S1=0, S0=0, I0=1  
Expected Output: Y=1  
<img width="1920" height="1032" alt="S1=0, S0=0, I0=1" src="https://github.com/user-attachments/assets/c28ebae0-cbb8-4b15-8f95-e0d8bda1edaa" />


### Test Case 2
S1=0, S0=1, I1=1  
Expected Output: Y=1  
<img width="1920" height="1032" alt="S1=0, S0=1, I1=1" src="https://github.com/user-attachments/assets/c0957421-c3a6-412c-9434-b668f25be4a3" />


### Test Case 3
S1=1, S0=0, I2=1  
Expected Output: Y=1  
<img width="1920" height="1032" alt="S1=1, S0=0, I2=1" src="https://github.com/user-attachments/assets/9c050d09-925b-4f92-990e-d5ac194aa94e" />


### Test Case 4
S1=1, S0=1, I3=1  
Expected Output: Y=1  
<img width="1920" height="1032" alt="S1=1, S0=1, I3=1" src="https://github.com/user-attachments/assets/55695ad0-4779-4cf9-ab08-65a881aa2d1b" />


## Conclusion
This project confirmed that a 4x1 multiplexer can be built entirely out of NOR gates. Even though it takes more gates compared to using mixed logic, it shows the power of universal gates and how any digital circuit can be reduced to just one gate type.

It was a fun experiment and a good way to practice gate-level design in Logisim Evolution.
