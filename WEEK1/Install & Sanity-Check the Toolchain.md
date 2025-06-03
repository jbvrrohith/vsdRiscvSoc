# 🚀 RISC-V Toolchain Setup Guide

This guide will help you install and verify the **RISC-V GNU Toolchain** (`rv32imac`) on a 64-bit Ubuntu system.

---

## 📦 Step 1: Extract the Toolchain

```bash
cd ~/Downloads
tar -xzvf riscv-toolchain-rv32imac-x86_64-ubuntu.tar.gz
```
## 🛠️ Step 2: Update Your PATH Variable
```bash
nano ~/.bashrc
```
Add the following line at the end:
```bash
export PATH="/home/jbvrrohith/Downloads/riscv/bin:$PATH"
```
## 💾 Step 3: Save and Apply

Save in nano: Ctrl + O, then Enter
Exit: Ctrl + X
```bash
source ~/.bashrc
```

## ✅ Step 4: Verify Installation
```bash
riscv32-unknown-elf-gcc --version
```
![GCC Version](./assets/o1.png)
```bash
riscv32-unknown-elf-objdump --version
```
![Objdump version](./assets/o2.png)
```bash
riscv32-unknown-elf-gdb --version
```
![GDB version](./assets/o3.png)
