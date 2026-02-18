| Opcode | Instruction | Description                             | ALU State |
|--------|-------------|-----------------------------------------|-----------|
| 0000   | (Spare)     | -                                       | -         |
| 0001   | (Spare)     | -                                       | -         |
| 0010   | (Spare)     | -                                       | -         |
| 0011   | (Spare)     | -                                       | -         |
| 0100   | JC          | Jump if Carry                           | Off       |
| 0101   | JZ          | Jump if Zero                            | Off       |
| 0110   | JL          | Jump if Less (< 0)                      | Off       |
| 0111   | JG          | Jump if Greater (>= 0)                  | Off       |
| 1000   | ADD         | Add A to B after a LDA                  | On        |
| 1001   | SUB         | Subtract B from A after a LDA           | On        |
| 1010   | AND         | AND A and B after a LDA                 | On        |
| 1011   | (Spare)     | -                                       | -         |
| 1100   | LDA         | Load A from memory                      | Off       |
| 1101   | LDB         | Load B from memory                      | Off       |
| 1110   | STA         | Store A to memory                       | Off       |
| 1111   | STS         | Store Sum to memory                     | Off       |
