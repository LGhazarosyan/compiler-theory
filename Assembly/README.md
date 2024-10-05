# Operations

Main Operations in assembly language use Stack. They use top elements from the stack, calculate the result value, pop them and push the resulting value. Assembly uses 3 types: BYTE, WORD, DWORD. For each command there is the alternative for each type. 

## Here are the commands supported by the Assembly.

- ADD|ADDW|ADDD - pops top 2 BYTE|WORD|DWORD and pushes the ADD result(If result overflows, sets the Z flag)
- SUB|SUBW|SUBD - pops top 2 BYTE|WORD|DWORD and pushes the SUB result(first popped - second popped)
- MUL|MULW|MULD - pops top 2 BYTE|WORD|DWORD and pushes MUL result. Top element is the LSB|LSW|LSD (least significant byte|word|dword). The second element is MSB|MSW|MSD
- DIV|DIVW|DIVD - pops top 2 BYTE|WORD|DWORD and pushes DIV result. Top element is the result, second element is reminder
- PUSH|PUSHW|PUSHD args - push given arguments as BYTE|WORD|DWORD
- POPD|POPW|POPD - pop from stack 1 BYTE|WORD|DWORD
- AND|ANDW|ANDD - pops top 2 BYTE|WORD|DWORD and pushes the AND result
- XOR|XORW|XORD - pops top 2 BYTE|WORD|DWORD and pushes the XOR result
- OR|ORW|ORD - pops top 2 BYTE|WORD|DWORD and pushes the OR result
- NOT|NOTW|NOTD - pops top BYTE|WORD|DWORD and pushes the NOT result
- CMP|CMPW|CMPD - compares top 2 elements of the Stack(top and second). The result if used in jumping expressions. If top > second JMPG will be executed. If equal the Z flag will be set
- JMP label - jump to label
- JMPG|JMPNE|JMPZ|JMPL|JMPLE|JMPGE label - jump to label if the condition is satisfied. The comparison should be just before the jump expression
- STOR|STORW|STORD ident - pops the stack element and stores it in ident.
- SHIFTL|SHIFTLW|SHIFTLD integer - pops top BYTE|WORD|DWORD and pushes the values left shifted by integer
- SHIFTR|SHIFTRW|SHIFTRD integer - pops top BYTE|WORD|DWORD and pushes the values left shifted by integer
- INPUT|INPUTW|INPUTD - takes input and pushes it to stack
- PRINT|PRINTW|PRINTD - pops the top stack element and prints it
- CP|CPW|CPD - copies the top element of stack and pushes to stack
- []|[]w|[]d integer - subscript operator. Uses top element as address to get the array element
