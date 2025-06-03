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
riscv32-unknown-elf-gcc  -o hello.elf hello.c
```
<details>
<summary><strong>riscv32-unknown-elf-gcc:</strong> This is the cross-compiler.</summary>
  
- **`riscv32`**: Specifies the target architecture – RISC-V 32-bit.
- **`unknown`**: Indicates that the vendor of the target system is unknown or not specified.
- **`elf`**: Specifies the output file format – Executable and Linkable Format (ELF), a common standard for executables and object code.
- **`gcc`**: Stands for GNU Compiler Collection, the actual compiler.
</details>
 

 
 <details>
<summary><strong>-o hello.elf:</strong> This is the output file flag.</summary>

- **`-o`**: Tells the compiler to place the output in the file that follows.  
- **`hello.elf`**: This will be the name of your compiled executable program.

</details>

<details>
<summary><strong>hello.c:</strong> This is your source code file.</summary>

- The C program you wrote in step 1.  
- It serves as the input for the compiler.

</details>

## Step 3: Verifying the Output 🧐

After running the compilation command, you use the `file` utility to check the generated file:
```bash
file hello.elf
```
The `file` command examines a file and tries to determine its type. 
![Output](./assets/p1.png)
