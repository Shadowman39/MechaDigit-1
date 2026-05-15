# Adding Numbers with MechaDigit-1

This program is meant to add one number to a starting number over and over, until the computer is turned off. We can set the starting value into one byte of RAM (RAM address 1, or RAM[1]) and the value to add repeatedly into another RAM byte (RAM address 0). After that the ROM is programmed with the four instructions described below.

---

## The Program

```assembly
1101 0000    LDB RAM[0]
1000 0001    ADD RAM[1]
1111 0001    STS RAM[1]
0111 0001    JG  ROM[1]
```

## Line-by-Line Explanation

### 1. `1101 0000` → **LDB RAM[0]**
- **Opcode**: 1101 = **LDB** (Load into B register)
- **Address**: 0000 = RAM location 0
- **What happens**: Copies the number stored in the first RAM slot (RAM[0]) into the **B register**.

The computer is preparing one number for addition.

### 2. `1000 0001` → **ADD RAM[1]**
- **Opcode**: 1000 = **ADD**
- **Address**: 0001 = RAM location 1
- **What happens**:
  - First loads the value from RAM[1] into register **A**
  - Then adds A + B together using the ALU

### 3. `1111 0001` → **STS RAM[1]**
- **Opcode**: 1111 = **STS** (Store Sum)
- **Address**: 0001 = RAM location 1
- **What happens**: Takes the result from the ALU and writes it back into RAM[1], replacing the old value.

The sum is now safely stored in memory.

### 4. `0111 0001` → **JG ROM[1]**
- **Opcode**: 0111 = **JG** (Jump if Greater or equal to zero)
- **Address**: 0001 = ROM location 1
- **What happens**: Checks the sign of the most recent result.
  - If the sum is **≥ 0** (positive or zero), the program jumps to instruction at ROM address 1.
  - If the sum is negative, it continues to the next instruction.
  - The sum is always positive since we're adding, so this acts as an unconditional jump to go back to the **ADD** instruction.

The program then continues until the user turns the computer off.
