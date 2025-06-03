# 📂Compile "Hello, RISC-V"
Converting the program wirtten in C language to machine readable language using GCC.

---

## Step 1: The C Program: hello.c C
Write the program in C language and save it.
```bash
#include <stdio.h>

int main() {
  printf("Hello, RISC-V");
  return 0;
}
```
## Step 2: The Compilation Command ⚙️
Compiling the C program
Open the terminal at your program directory 
```bash
riscv32-unknown-elf-gcc -march=rv32imc -mabi=ilp32 -o hello.elf hello.c
```
riscv32-unknown-elf-gcc: This is the cross-compiler.
<details>
<summary><strong>-march=rv32imc:</strong> This flag specifies the target microarchitecture.</summary>
  rv32i: This is the base 32-bit RISC-V integer instruction set.
  m: This indicates support for integer multiplication and division instructions.
  c: This indicates support for compressed instructions (which help reduce code size). 
  So, you're telling the compiler to generate code compatible with a RISC-V processor that has these specific features.
</details>

<hr>
 
-mabi=ilp32: This flag sets the Application Binary Interface (ABI).
  
