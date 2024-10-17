### 1. **Data Movement Instructions**
   - `MOV` – Move data
   - `PUSH` – Push data onto the stack
   - `POP` – Pop data from the stack
   - `LEA` – Load effective address
   - `XCHG` – Exchange data
   - `IN` / `OUT` – Input/output from/to port
   - `PUSHA` / `POPA` – Push/pop all general-purpose registers
   - `MOVSB`, `MOVSW`, `MOVSD` – Move byte, word, or doubleword
   - `PUSHF` / `POPF` – Push/pop flags onto/from the stack
   - `LAHF` / `SAHF` – Load/Store flags into/from AH register
   - `CMOVcc` – Conditional move instructions based on status flags

### 2. **Arithmetic Instructions**
   - `ADD` – Add
   - `SUB` – Subtract
   - `MUL` – Unsigned multiply
   - `IMUL` – Signed multiply
   - `DIV` – Unsigned divide
   - `IDIV` – Signed divide
   - `INC` – Increment
   - `DEC` – Decrement
   - `ADC` – Add with carry
   - `SBB` – Subtract with borrow
   - `NEG` – Two's complement negation
   - `CMP` – Compare (like subtract but result isn’t stored)
   - `TEST` – Bitwise compare (like AND but result isn’t stored)
   - `AAA`, `AAS`, `DAA`, `DAS` – ASCII/Binary adjust after arithmetic

### 3. **Bitwise Logical Instructions**
   - `AND` – Bitwise AND
   - `OR` – Bitwise OR
   - `XOR` – Bitwise XOR
   - `NOT` – Bitwise NOT
   - `SHL` / `SAL` – Shift left / Shift arithmetic left
   - `SHR` – Shift right
   - `SAR` – Shift arithmetic right
   - `ROL` / `ROR` – Rotate left / Rotate right
   - `RCL` / `RCR` – Rotate through carry left/right
   - `BT` / `BTS` / `BTR` / `BTC` – Bit test and set/reset/compliment
   - `BSF` / `BSR` – Bit scan forward / reverse

### 4. **Control Flow Instructions**
   - **Unconditional Jumps:**
     - `JMP` – Unconditional jump
     - `CALL` – Call procedure
     - `RET` – Return from procedure
     - `JMP FAR` – Jump to a far memory address
     - `ENTER` / `LEAVE` – Set up / exit stack frame

   - **Conditional Jumps:**
     - `JE` / `JZ` – Jump if equal / zero
     - `JNE` / `JNZ` – Jump if not equal / not zero
     - `JA` / `JNBE` – Jump if above (unsigned) / not below or equal
     - `JAE` / `JNB` – Jump if above or equal (unsigned) / not below
     - `JB` / `JNAE` – Jump if below (unsigned) / not above or equal
     - `JBE` / `JNA` – Jump if below or equal (unsigned) / not above
     - `JG` / `JNLE` – Jump if greater (signed) / not less or equal
     - `JGE` / `JNL` – Jump if greater or equal (signed) / not less
     - `JL` / `JNGE` – Jump if less (signed) / not greater or equal
     - `JLE` / `JNG` – Jump if less or equal (signed) / not greater
     - `JO` – Jump if overflow
     - `JNO` – Jump if not overflow
     - `JS` – Jump if sign (negative)
     - `JNS` – Jump if not sign (positive)
     - `JP` / `JPE` – Jump if parity even
     - `JNP` / `JPO` – Jump if not parity / parity odd
     - `JC` – Jump if carry
     - `JNC` – Jump if not carry

   - **Loop and Repeat Instructions:**
     - `LOOP` – Loop with CX/ECX as counter
     - `LOOPE` / `LOOPZ` – Loop while equal / zero
     - `LOOPNE` / `LOOPNZ` – Loop while not equal / not zero
     - `JCXZ` / `JECXZ` – Jump if CX / ECX is zero

### 5. **String Manipulation Instructions**
   - `MOVS` – Move string data
   - `LODS` – Load string data
   - `STOS` – Store string data
   - `SCAS` – Scan string data
   - `CMPS` – Compare strings
   - `REP` – Repeat string instruction
   - `REPE` / `REPZ` – Repeat while equal / zero
   - `REPNE` / `REPNZ` – Repeat while not equal / not zero

### 6. **Floating-Point Instructions (x87 FPU)**
   - `FLD` – Load floating-point value
   - `FST` – Store floating-point value
   - `FADD` – Add floating-point
   - `FSUB` – Subtract floating-point
   - `FMUL` – Multiply floating-point
   - `FDIV` – Divide floating-point
   - `FSTP` – Store floating-point and pop
   - `FXCH` – Exchange floating-point registers
   - `FSTCW` – Store control word
   - `FNSTSW` – Store status word
   - `FINIT` – Initialize FPU

### 7. **SIMD Instructions (SSE, AVX, etc.)**
   - `MOVAPS` / `MOVUPS` – Move aligned/unaligned packed single-precision data
   - `ADDPS` / `ADDSS` – Add packed / scalar single-precision data
   - `SUBPS` / `SUBSS` – Subtract packed / scalar single-precision data
   - `MULPS` / `MULSS` – Multiply packed / scalar single-precision data
   - `DIVPS` / `DIVSS` – Divide packed / scalar single-precision data
   - `CVTSS2SD` – Convert scalar single-precision to double-precision
   - `PXOR` – Packed bitwise XOR
   - `PAND` – Packed bitwise AND
   - `MOVDQA` / `MOVDQU` – Move aligned / unaligned packed integer data
   - `PSLLDQ` / `PSRLDQ` – Shift left / right logical for quadword

### 8. **System Instructions**
   - `HLT` – Halt the CPU
   - `INT` – Trigger interrupt
   - `IRET` – Return from interrupt
   - `CLI` / `STI` – Clear/set interrupt flag
   - `INVLPG` – Invalidate page table entry
   - `LGDT` / `LIDT` – Load global/interrupt descriptor table
   - `SGDT` / `SIDT` – Store global/interrupt descriptor table
   - `SMSW` – Store machine status word
   - `LMSW` – Load machine status word
   - `CLTS` – Clear task-switched flag
   - `CPUID` – CPU identification

### 9. **Virtualization Instructions (VMX, SVM)**
   - `VMXON` / `VMXOFF` – Enable/disable VMX operation
   - `VMCALL` – Call to virtual machine monitor
   - `VMREAD` / `VMWRITE` – Read/write VMCS field
   - `VMLAUNCH` / `VMRESUME` – Launch/resume VM

### 10. **Miscellaneous Instructions**
   - `NOP` – No operation
   - `PAUSE` – Hint to reduce power consumption in spin-wait loops
   - `XLAT` – Translate byte to byte table lookup
   - `BSF` / `BSR` – Bit scan forward / reverse
   - `RDTSC` – Read time-stamp counter
   - `RDRAND` / `RDSEED` – Read random number
   - `SYSENTER` / `SYSEXIT` – Fast system call/sysret
