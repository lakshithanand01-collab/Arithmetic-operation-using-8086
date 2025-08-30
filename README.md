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
|<img width="640" height="480" alt="Screenshot (7)" src="https://github.com/user-attachments/assets/01f65334-66ff-4264-a5b1-7df651705192" />|<img width="640" height="480" alt="Screenshot (6)" src="https://github.com/user-attachments/assets/20777f3a-ba72-47f4-8951-eb7437d6fd36" />

#### Manual Calculations

(![WhatsApp Image 2025-08-30 at 12 52 05_ba957d4a](https://github.com/user-attachments/assets/b6a32df6-cd94-4fd2-9152-89f6180d9377)
)

---

## OUTPUT IMAGE FROM MASM SOFTWARE

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



#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|<img width="1271" height="809" alt="Screenshot 2025-08-30 124725" src="https://github.com/user-attachments/assets/5742449b-beda-47d6-bddb-95cd47683c80" />|<img width="1264" height="859" alt="Screenshot 2025-08-30 124739" src="https://github.com/user-attachments/assets/6dd52ebd-5eec-4dcd-9ec9-f7e02fd87c20" />|

#### Manual Calculations

(![WhatsApp Image 2025-08-30 at 12 54 05_04f070c9](https://github.com/user-attachments/assets/edcbf540-af35-442e-801b-ca7e938313a6)
)

---


## OUTPUT SCREEN FROM MASM SOFTWARE

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
|<img width="651" height="422" alt="Screenshot 2025-08-25 135416" src="https://github.com/user-attachments/assets/df9151c9-87a6-4dc0-911c-0535c470b4c1" />|<img width="641" height="435" alt="Screenshot 2025-08-25 135444" src="https://github.com/user-attachments/assets/9f98b0dc-f446-4759-b35f-81c31d0cba21" />|

#### Manual Calculations

(![WhatsApp Image 2025-08-30 at 12 58 09_96ae8c9c](https://github.com/user-attachments/assets/4dea862b-c454-4311-802e-461d178289a8)
)

---

## OUTPUT SCREEN FROM MASM SOFTWARE

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
|<img width="640" height="480" alt="Screenshot (9)" src="https://github.com/user-attachments/assets/ffaf86c3-af04-4af0-b82e-9c37e8476f5b" /> |<img width="640" height="480" alt="Screenshot (8)" src="https://github.com/user-attachments/assets/75bbc7f0-c82e-47b6-9f35-64ce3df62d0e" /> |

#### Manual Calculations

(![WhatsApp Image 2025-08-30 at 13 00 29_0c287fef](https://github.com/user-attachments/assets/3aa985a8-2263-4923-b94a-cd589914888b)
)

---
## OUTPUT FROM MASM SOFTWARE



## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
