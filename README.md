# MPMC-EXPT-1-ARITHMETIC-OPERATIONS-USING-8086
AIM:-

To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

APPARATUS REQUIRED
Personal Computer with MASM Software

1. ADDITION
2. 
Algorithm

1.Initialize memory location in HL register.

2.Store 1st data.

3.Increment HL to enter 2nd data.

4.Move 2nd number to accumulator.

5.Decrement HL.

6.Add value in memory with accumulator.

7.Store result.

8.Stop.

FLOW CHART:-

<img width="707" height="1024" alt="image" src="https://github.com/user-attachments/assets/94ac1a93-843d-405f-a9b0-e4b5a26b1d9d" />

PROGRAM:-

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

OUTPUT TABLE:-

| MEMORY LOCATION(INPUT)|MEMORY LOCATION(OUTPUT)|
|-----------------------|-----------------------|
|1201:34                |68:1205                |
|1202:12                |00:1206                |
|1203:34                |c4:1207                |

OUTPUT FROM MASM SOFTWARE:-

![WhatsApp Image 2026-02-02 at 11 34 00](https://github.com/user-attachments/assets/c9485c63-c906-45f9-b083-f33438197dbc)

MANUAL CALCULATION:-

<img width="1280" height="717" alt="image" src="https://github.com/user-attachments/assets/91f63504-3c21-40c2-85c5-923a8ccd8d16" />

 
2. SUBTRACTION

Algorithm

1.Initialize memory and store 1st data.

2.Increment to get 2nd data.

3.Move 2nd data to accumulator.

4.Subtract memory content.

5.Store result.


FLOWCHART:-

<img width="578" height="797" alt="image" src="https://github.com/user-attachments/assets/93af8d88-c1dc-4080-8b48-8a9e34b83bec" />

PROGRAM:-

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


OUTPUT TABLE:-


| MEMORY LOCATION(INPUT)|MEMORY LOCATION(OUTPUT)|
|-----------------------|-----------------------|
|1201:34                |68:1205                |
|1202:12                |00:1206                |
|1203:34                |c4:1207                |

MANUAL CALCULATION:-

<img width="1280" height="717" alt="image" src="https://github.com/user-attachments/assets/5b8f5948-0aad-48ba-8ef5-f6e9c30e4e0c" />


OUTPUT SCREEN FROM MASM SOFTWARE:-

![WhatsApp Image 2026-02-02 at 11 33 49](https://github.com/user-attachments/assets/cad48761-1775-4bdc-92a3-2096bc0ff8f3)


3. MULTIPLICATION

Algorithm

1.Initialize memory and store operands.

2.Move operands to registers.

3.Multiply.

4.Store result.


FLOW CHART :-

<img width="569" height="906" alt="image" src="https://github.com/user-attachments/assets/f4a48e88-707c-4c4c-b492-aa7b32ab4a10" />

PROGRAM:-

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

OUTPUT TABLE:-

| MEMORY LOCATION(INPUT)|MEMORY LOCATION(OUTPUT)|
|-----------------------|-----------------------|
|1201:34                |68:1205                |
|1202:12                |00:1206                |
|1203:34                |c4:1207                |

MANUAL CALCULATIONS:-

<img width="1280" height="717" alt="image" src="https://github.com/user-attachments/assets/05475411-3916-4fd0-bee6-ba1f417c9b90" />

OUTPUT SCREEN FROM MASM SOFTWARE:-

<img width="904" height="566" alt="image" src="https://github.com/user-attachments/assets/0a3581f7-a08f-45a0-952d-8c991fe610b9" />


4. DIVISION
   
Algorithm

1.Load memory location of operands.

2.Perform division.

3.Store result.

FLOWCHART:-

<img width="1065" height="802" alt="image" src="https://github.com/user-attachments/assets/ac85c70f-99c8-4097-b9c4-f8ede31f17e7" />

PROGRAM:-

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

OUTPUT TABLE:-

| MEMORY LOCATION(INPUT)|MEMORY LOCATION(OUTPUT)|
|-----------------------|-----------------------|
|1201:34                |68:1205                |
|1202:12                |00:1206                |
|1203:34                |c4:1207                |

MANUAL CALCULATIONS:-

![WhatsApp Image 2026-02-04 at 10 29 37](https://github.com/user-attachments/assets/7d3cd0ff-ef40-4b90-bec1-d7561b59ffcc)


OUTPUT SCREEN FROM MASM SOFTWARE:-

![WhatsApp Image 2026-02-02 at 11 34 16](https://github.com/user-attachments/assets/1f1cb6b4-386d-45f3-9c13-797c4f6700b1)


RESULT:-

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.






















