 #  ABI & Register Cheat-Sheet

 <details><summary><b>Step 1: List all 32 RV32 integer registers with their ABI names</b></summary><br>


| Register | ABI Name | Typical Role                      |
|----------|----------|---------------------------------|
| x0       | zero     | Hard-wired zero (always 0)      |
| x1       | ra       | Return address                  |
| x2       | sp       | Stack pointer                  |
| x3       | gp       | Global pointer                 |
| x4       | tp       | Thread pointer                 |
| x5       | t0       | Temporary / caller-saved       |
| x6       | t1       | Temporary / caller-saved       |
| x7       | t2       | Temporary / caller-saved       |
| x8       | s0/fp    | Saved register / frame pointer |
| x9       | s1       | Saved register                 |
| x10      | a0       | Function argument / return     |
| x11      | a1       | Function argument / return     |
| x12      | a2       | Function argument              |
| x13      | a3       | Function argument              |
| x14      | a4       | Function argument              |
| x15      | a5       | Function argument              |
| x16      | a6       | Function argument              |
| x17      | a7       | Function argument              |
| x18      | s2       | Saved register                 |
| x19      | s3       | Saved register                 |
| x20      | s4       | Saved register                 |
| x21      | s5       | Saved register                 |
| x22      | s6       | Saved register                 |
| x23      | s7       | Saved register                 |
| x24      | s8       | Saved register                 |
| x25      | s9       | Saved register                 |
| x26      | s10      | Saved register                 |
| x27      | s11      | Saved register                 |
| x28      | t3       | Temporary / caller-saved       |
| x29      | t4       | Temporary / caller-saved       |
| x30      | t5       | Temporary / caller-saved       |
| x31      | t6       | Temporary / caller-saved       |

</details>

<details><summary><b>Step 2: Calling Convention Summary</b></summary>

- **a0–a7 (x10–x17):** Used to pass function arguments and return values.  
- **s0–s11 (x8, x9, x18–x27):** Callee-saved registers. The function must save and restore these if it modifies them.  
- **t0–t6 (x5–x7, x28–x31):** Caller-saved temporaries. The caller must save these if needed after a function call.  
- **ra (x1):** Return address. Used to store the address to return to after a function call.  
- **sp (x2):** Stack pointer. Points to the current top of the stack.  
- **gp (x3):** Global pointer. Used for accessing global variables in some environments.  
- **tp (x4):** Thread pointer. Used for thread-local storage.  
- **zero (x0):** Always zero. Writes have no effect.

</details>
