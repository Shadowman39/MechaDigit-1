| Opcode | Instruction | Description                     | ALU State |
|--------|-------------|---------------------------------|-----------|
| 0000   | ADD         | Add A to B after a LDA          | On        |
| 0001   | SUB         | Subtract B from A after a LDA   | On        |
| 0010   | AND         | AND A and B after a LDA         | On        |
| 0011   | (Spare)     | -                               | -         |
| 0100   | LDA         | Load A from memory              | Off       |
| 0101   | LDB         | Load B from memory              | Off       |
| 0110   | STA         | Store A to memory               | Off       |
| 0111   | STS         | Store Sum to memory             | Off       |
| 1000   | (Spare)     | -                               | -         |
| 1001   | (Spare)     | -                               | -         |
| 1010   | (Spare)     | -                               | -         |
| 1011   | (Spare)     | -                               | -         |
| 1100   | JC          | Jump if Carry                   | Off       |
| 1101   | JZ          | Jump if Zero                    | Off       |
| 1110   | JL          | Jump if Less (< 0)              | Off       |
| 1111   | JG          | Jump if Greater (>= 0)          | Off       |
