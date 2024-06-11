# This processor has been made to allow the execution of very simple programs and to learn the basics of a processor.
Made using CircuitVerse, here is my project: https://circuitverse.org/simulator/edit/cpu-nano-8-bits

![cpu_8_bits_final](https://github.com/SebHub7/8-bits-processor/assets/160337978/0079dfc3-871c-4e0d-a260-0a8dbb460fdd)


# Features:
  - 8 bits CPU
  - 16 bytes ROM
  - 32 bytes RAM
  - No registers (just the accumulator to save results from one operation to another)

# Instruction set:
3 bits for the operation code and 5 bits for the operand (value or RAM/ROM address)

| Short instruction | Instruction | Operation code | Operand |
| --- | --- | --- | --- |
| LV | Load Value | 000 | 5 bits specifying the RAM address storing the value we want to load |
| SV | Store Value | 001 | 5 bits specifying the RAM address where we want to store the accumulator value |
| ADD | Addition | 010 | 5 bits specifying a value |
| ADDA | Addition | 011 | 5 bits specifying a RAM address, the value stored at that address will be added to the accumulator (necessary because the processor only have one register) |
| J | Jump | 100 | 5 bits specifying the ROM address to jump to |

# Fibonacci program coded in the ROM
| Assembly code | Binary code | 
| --- | --- |
| LV 0x0 | 000 00000 |
| ADD 1 | 010 00001 |
| SV 0x0 | 001 00000 |
| LV 0x0 | 000 00000 |
| SV 0x2 | 001 00010 |
| ADDA 0x1 | 011 00001 |
| SV 0x0 | 001 00000 |
| LV 0x2 | 000 00010 |
| SV 0x1 | 001 00001 |
| J 0x3 | 100 00011 |
