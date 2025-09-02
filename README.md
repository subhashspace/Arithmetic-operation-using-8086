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
<img width="500" height="550" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,1200H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
ADD AX,BX
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

______________________________________________________
| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|     1200                |         1204             |
|     1201                |         1205             |
|     1202                |                          |
|     1203                |                          |


#### Manual Calculations

<img width="450" height="500" alt="Screenshot 2025-09-02 200337" src="https://github.com/user-attachments/assets/2f93e23f-e6a6-4bf3-b031-f2554d28a1c2" />




---

## OUTPUT IMAGE FROM MASM SOFTWARE

<img width="550" height="600" alt="Screenshot (1)" src="https://github.com/user-attachments/assets/04b53cf6-409b-433b-8bcf-86cd340d68b9" />


## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="500" height="550" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


#### Program

```asm
CODE SEGMENT
ASSUME CS:CODE,DS:CODE
ORG 1000H
MOV SI,1200H
MOV AX,[SI]
MOV BX,[SI+02H]
MOV CL,00H
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

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|        1200             |                          |
|        1201             |           1204           |
|        1202             |           1205           |
|        1203             |                          |

#### Manual Calculations

<img width="450" height="500" alt="Screenshot 2025-09-02 200702" src="https://github.com/user-attachments/assets/b27ebc9d-4d70-4750-8d0f-0e87bffe8b1b" />



---


## OUTPUT SCREEN FROM MASM SOFTWARE


<img width="550" height="600" alt="Screenshot (2)" src="https://github.com/user-attachments/assets/afc98933-0c00-4272-967f-f043233e35d3" />



## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

<img width="500" height="550" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,1200H
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

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|         1200            |           1204           |
|         1201            |           1205           |
|         1202            |           1206           |
|         1203            |           1207           |

#### Manual Calculations

<img width="450" height="500" alt="Screenshot 2025-09-02 200950" src="https://github.com/user-attachments/assets/bfbb1dc2-0d74-4c06-bc59-02e19a53ea28" />



---

## OUTPUT SCREEN FROM MASM SOFTWARE


<img width="550" height="600" alt="Screenshot (3)" src="https://github.com/user-attachments/assets/37ea2310-b82b-448c-bdeb-0f5751ad281c" />



## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART
<img width="500" height="550" alt="image" src="https://github.com/user-attachments/assets/25b4a483-0d42-494b-8639-1af3ea17191b" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,1200H
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

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|         1200            |           1204           |
|         1201            |           1205           |
|         1202            |           1206           |
|         1203            |           1207           |

#### Manual Calculations

<img width="450" height="500" alt="image" src="https://github.com/user-attachments/assets/135e8a56-e605-4e82-a4c9-777c536105c0" />



---
## OUTPUT FROM MASM SOFTWARE


<img width="550" height="600" alt="Screenshot (4)" src="https://github.com/user-attachments/assets/4f15918b-3417-4502-bbee-c4d3c78eb1a6" />




## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
