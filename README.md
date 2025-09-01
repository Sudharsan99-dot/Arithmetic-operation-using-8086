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
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
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

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|           2000 : 56     |              2004 : 68   |
2001 : 78 | 2005 : AC
2002 : 12 | 2006 : 00
2003 : 34 | 2007 : D6
#### Manual Calculations

(Add your calculation here)

---![sadd](https://github.com/user-attachments/assets/06ee92fb-5f87-4155-8922-e3f4092af2fb)


## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="642" height="427" alt="sudh_add" src="https://github.com/user-attachments/assets/8f1e5540-87b6-446a-bb1e-5c8ff46072d6" />

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

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|             2000 : 56   |   2004 : 44              |
2001 : 78 | 2005 : 44
2002 : 12 | 2006 : 00
2003 : 34 | 2007 : D6
#### Manual Calculations

(Add your calculation here)

---
![ssub](https://github.com/user-attachments/assets/a76c5de9-e07d-4b85-badf-df86ac2c8a3a)


## OUTPUT SCREEN FROM MASM 
<img width="642" height="427" alt="sudh_sub" src="https://github.com/user-attachments/assets/433fcbed-08bd-4fcb-b942-6888bb228edc" />
SOFTWARE

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

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|            2000 : 12    |         2004 : 44        |
2001 : 34 | 2005 : 51
2002 : 12 | 2006 : 97
2003 : 34 | 2007 : 0A
#### Manual Calculations

(Add your calculation here)

---![smul](https://github.com/user-attachments/assets/d359aa94-f81b-4f7d-b67f-0bf96074f73f)


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="642" height="427" alt="sudh_mul" src="https://github.com/user-attachments/assets/15310eea-13c2-44c0-975d-5871cbd052d6" />

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

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|            2000 : 12    |          2004 : 01            |
2001 : 34 | 2005 : 00
2002 : 12 | 2006 : 00
2003 : 34 | 2007 : 00
#### Manual Calculations

(Add your calculation here)
![sdiv](https://github.com/user-attachments/assets/6756d89a-f539-4592-b4f4-cc13a23636d2)

---
## OUTPUT FROM MASM SOFTWARE

<img width="642" height="427" alt="sudh_div" src="https://github.com/user-attachments/assets/42c10e4f-7379-4841-84e9-158682d6ae08" />


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
