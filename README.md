# Arithmetic-operation-using-8086
# 8086 Assembly Language Programs for Arithmetic Operations

## AIM

To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

---

## APPARATUS REQUIRED

* Personal Computer with MASM Software

---

## 1. ADDITION

#### Algorithm

1. Initialize memory location in HL register.
2. Store 1st data.
3. Increment HL to enter 2nd data.
4. Move 2nd number to accumulator.
5. Decrement HL.
6. Add value in memory with accumulator.
7. Store result.
8. Stop.


## FLOW CHART
<img width="707" height="1024" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


#### Program

```asm
CODE SEGMENT
ASSUME CS:CODE, DS:CODE
ORG 1000H
MOV CL,00H
MOV AX,1234H
MOV BX,1234H
ADD AX,BX
JNC L1
INC CL
L1:MOV SI,1200H
MOV [SI],AX
MOV [SI+2],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|       1200🔢       01         12

|         1200                    |

#### Manual Calculations

<img width="640" height="400" alt="image" src="https://github.com/user-attachments/assets/6739aae7-df48-4ce1-b36d-8f0afe8fe233" />


---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="640" height="400" alt="image" src="https://github.com/user-attachments/assets/67b782e1-e888-42aa-aa7d-c2fcdb053d44" />


## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="578" height="797" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


#### Program
```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
SUB AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```


#### Output Table

<img width="744" height="296" alt="image" src="https://github.com/user-attachments/assets/5c52d5fd-3964-48aa-98ed-14f226e2c5d9" />

#### Manual Calculations

<img width="1409" height="1599" alt="image" src="https://github.com/user-attachments/assets/dcbfe208-25de-4c42-ba29-6661347b66a1" />


---


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="640" height="400" alt="image" src="https://github.com/user-attachments/assets/2daeeb6d-08bf-4836-a8e5-bb6517102537" />


## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

<img width="569" height="906" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
MUL BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

<img width="746" height="296" alt="image" src="https://github.com/user-attachments/assets/11b570c7-5a55-4ba2-acb6-f836e72be66a" />


#### Manual Calculations

<img width="640" height="400" alt="image" src="https://github.com/user-attachments/assets/6f1ba8b1-cbb0-432e-bc2f-322fa0abe65a" />


---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="1160" height="1374" alt="image" src="https://github.com/user-attachments/assets/cb3ab9ce-2545-4cb0-ad25-704ba5373ca2" />


## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART
<img width="1065" height="802" alt="image" src="https://github.com/user-attachments/assets/25b4a483-0d42-494b-8639-1af3ea17191b" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
DIV BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

<img width="748" height="302" alt="image" src="https://github.com/user-attachments/assets/601e9f54-68ed-4299-922a-bb87699bf349" />


#### Manual Calculations

<img width="1600" height="1600" alt="image" src="https://github.com/user-attachments/assets/cc60e9fb-60c5-4cff-84d3-382e86f18e18" />


---
## OUTPUT FROM MASM SOFTWARE

<img width="1350" height="1600" alt="image" src="https://github.com/user-attachments/assets/7e565a72-3436-445c-a450-3a1d7d0584e0" />


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

