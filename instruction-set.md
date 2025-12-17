| Opcode | Instruction | Description                     | ALU State |
|--------|-------------|---------------------------------|-----------|
| 0000   | LDA         | Load A from memory              | Off       |
| 0001   | LDB         | Load B from memory              | Off       |
| 0010   | STA         | Store A to memory               | Off       |
| 0011   | STS         | Store Sum to memory             | Off       |
| 0100   | ADD         | Add A to B after a LDA          | On        |
| 0101   | SUB         | Subtract B from A after a LDA   | On        |
| 0110   | AND         | AND A and B after a LDA         | On        |
| 0111   | (Spare)     | -                               | -         |
| 1000   | JC          | Jump if Carry                   | Off       |
| 1001   | JZ          | Jump if Zero                    | Off       |
| 1010   | JL          | Jump if Less (< 0)              | Off       |
| 1011   | JG          | Jump if Greater (>= 0)          | Off       |
| 1100   | (Spare)     | -                               | -         |
| 1101   | (Spare)     | -                               | -         |
| 1110   | DISPLAY     | Output Sum to display           | Off       |
| 1111   | HALT        | Stop execution                  | Off       |
