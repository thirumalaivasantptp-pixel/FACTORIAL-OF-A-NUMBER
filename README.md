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


<img width="620" height="336" alt="image" src="https://github.com/user-attachments/assets/9c7fbe12-6ca9-4388-9542-e1c99163d186" />
<img width="540" height="353" alt="image" src="https://github.com/user-attachments/assets/6918c79a-9e48-4c4d-924d-6db3be6d577b" />


MANUAL CALCULATIONS


<img width="405" height="384" alt="image" src="https://github.com/user-attachments/assets/d9fd36e5-390f-42b2-8202-72c8bff63312" />

---

RESULT

Thus, the factorial of a number was calculated and executed successfully using 8051 Keil.

---


