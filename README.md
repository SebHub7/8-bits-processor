# This processor has been made to allow the execution of very simple programs and to learn the basics of a processor.

![cpu_8_bits_final](https://github.com/SebHub7/8-bits-processor/assets/160337978/0079dfc3-871c-4e0d-a260-0a8dbb460fdd)


# Features:
  - 8 bits CPU
  - 16 bytes ROM
  - 32 bytes RAM
  - One register (accumulator)
  - Fibonacci program already coded

# Instruction set:
  - 3 bits for operand code | 5 bits for value / RAM address
  - LV | Load Value | opcode: 000 + 5 bits specifying the RAM address storing the value we want to load
  - SV | Store Value | opcode: 001 + 5 bits specifying the RAM address where we want to store the accumulator value
  - ADD | addition | opcode: 010 + 5 bits specifying a value
  - ADDA | addition | opcode: 011 + 5 bits specifying a RAM address, the value stored at that address will be added to the accumulator (necessary because the processor only have one register)
  - J | jump | opcode: 100 + 5 bits specifying the ROM address to jump to
