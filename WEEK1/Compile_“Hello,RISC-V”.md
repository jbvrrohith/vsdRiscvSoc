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
  rv32i: This is the base 32-bit RISC-V integer instruction set.\n
  m: This indicates support for integer multiplication and division instructions.\n
  c: This indicates support for compressed instructions (which help reduce code size). \n
  So, you're telling the compiler to generate code compatible with a RISC-V processor that has these specific features.
</details>
<details>
<summary><strong>-mabi=ilp32:</strong> This flag sets the Application Binary Interface (ABI).</summary>
  ilp32: Stands for "Integer, Long, Pointer are 32-bit". This defines how data types are represented in memory and how function calls are made. It means int, long, and pointers are all 32 bits wide on this target.
 </details>
