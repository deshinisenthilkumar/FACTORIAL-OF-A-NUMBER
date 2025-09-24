# FACTORIAL-OF-A-NUMBER
# FACTORIAL OF A NUMBER USING 8051 (Keil)

## AIM
To write and execute an Assembly language program to perform the factorial of a number using 8051 Keil.

---

## APPARATUS REQUIRED
- Personal computer with Keil software

---

## ALGORITHM
1. **Start**
2. **Input**: Read the number `n`.
3. **Initialize**:
   - Set factorial to `1`.
   - Set `i` to `1`.
4. **Loop**: While `i` is less than or equal to `n`:
   - Multiply factorial by `i`.
   - Increment `i` by `1`.
5. **Output**: Store or print the value of factorial.
6. **End**

---

## FLOWCHART
<img width="506" height="525" alt="image" src="https://github.com/user-attachments/assets/f3b47187-6f0f-490c-8704-f2973cb2b276" />


---

## PROGRAM
```asm
ORG 0000H
MOV DPTR,#4500H
MOVX A,@DPTR
MOV R0,A
INC DPTR
ACALL FACTORIAL
MOVX @DPTR,A
SJMP THIN
FACTORIAL:DEC R0
CJNE R0,#01H,PRODUCT
SJMP THICK
PRODUCT:MOV B,R0
MUL AB
ACALL FACTORIAL
THICK: RET
THIN:RET
END

```
OUTPUT

<img width="400" height="500" alt="Screenshot 2025-09-24 210529" src="https://github.com/user-attachments/assets/2bad6ebd-50ac-4ebd-88c1-1a17cc25cf7e" />

<img width="700" height="400" alt="Screenshot 2025-09-24 211813" src="https://github.com/user-attachments/assets/ec7fec5b-bfd6-4757-af4f-a37d6c4bbd34" />

---
MANUAL CALCULATIONS

![WhatsApp Image 2025-09-24 at 21 36 58_3c4cc9f2](https://github.com/user-attachments/assets/8075006a-a51e-41f0-b44f-68cc62ee28f4)


RESULT

Thus, the factorial of a number was calculated and executed successfully using 8051 Keil.

---


