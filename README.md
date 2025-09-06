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

<img width="638" height="246" alt="image" src="https://github.com/user-attachments/assets/9a18c9d7-29d8-49cd-98cc-6cc59efa8f56" />


#### Manual Calculations

<img width="833" height="589" alt="image" src="https://github.com/user-attachments/assets/081b55d4-41ed-4543-b37a-d40105283ea9" />

---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="643" height="433" alt="Screenshot 2025-09-06 103114" src="https://github.com/user-attachments/assets/d0728b69-c8ce-438a-813b-3a26914d6f5a" />
<img width="643" height="403" alt="Screenshot 2025-09-06 081849" src="https://github.com/user-attachments/assets/53c3997d-b846-4556-b504-9dd8f1ab32d2" />

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

<img width="656" height="243" alt="image" src="https://github.com/user-attachments/assets/b2d582c1-a547-416d-a3db-d1272598d476" />


#### Manual Calculations

<img width="715" height="752" alt="image" src="https://github.com/user-attachments/assets/be30f2e2-d360-4e0f-97cf-abdb4734a36d" />


---


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="634" height="425" alt="Screenshot 2025-09-06 103138" src="https://github.com/user-attachments/assets/abe75190-66e9-472e-83d5-3a9007a1a21c" />
<img width="640" height="426" alt="Screenshot 2025-09-06 103011" src="https://github.com/user-attachments/assets/ee34932f-f7a0-4ec9-9ce5-84f7c21b846d" />


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

<img width="676" height="263" alt="image" src="https://github.com/user-attachments/assets/bdf51fdc-b410-4b5d-b7d2-946aa58f6099" />


#### Manual Calculations

<img width="670" height="702" alt="image" src="https://github.com/user-attachments/assets/49242aa1-0a15-4c90-9792-eb69c60e7d30" />


---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="649" height="428" alt="Screenshot 2025-09-06 104104" src="https://github.com/user-attachments/assets/2141f306-a3ea-4494-acd2-026bb631766a" />
<img width="625" height="443" alt="Screenshot 2025-09-06 104007" src="https://github.com/user-attachments/assets/b4d52859-39c6-4c1b-ab9f-87ab2b12ee0c" />



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
<img width="674" height="253" alt="image" src="https://github.com/user-attachments/assets/0e2d86db-cb30-4c59-8bc5-2a2321cd92ec" />


#### Manual Calculations

<img width="645" height="617" alt="image" src="https://github.com/user-attachments/assets/a3871ffb-1e7c-402a-ba7a-5bc3826b978f" />


---
## OUTPUT FROM MASM SOFTWARE
<img width="640" height="430" alt="Screenshot 2025-09-06 104813" src="https://github.com/user-attachments/assets/a7c65e45-fb21-4aa5-bf5a-2ac94db1a3f2" />
<img width="652" height="431" alt="Screenshot 2025-09-06 104719" src="https://github.com/user-attachments/assets/a0855ed3-b07f-47a4-b1ed-cb01f117ec5f" />




## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
