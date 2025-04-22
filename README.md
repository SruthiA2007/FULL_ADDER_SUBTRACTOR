# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

FULL ADDER
![image](https://github.com/user-attachments/assets/5ffb9aa3-0df1-4b15-b943-bd11e5f62a51)

FULL SUBTRACTOR
![Screenshot 2025-04-22 223146](https://github.com/user-attachments/assets/deb5ba51-ae44-426f-9f02-1864520174ab)

**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: SRUTHI A

RegisterNumber: 212224240162
*/
FULL ADDER

module fulladder(a,b,cin,sum,carry);

input a,b,cin;

output sum,carry;

assign sum=( (a ^ b)^cin);

assign carry= ( (a & b)| ( cin &(a ^ b )));

endmodule

FULL SUBTRACTOR

module fs(a,b,bin,difference,borrow);

input a,b,bin;

output difference,borrow;

assign difference= ( (a ^ b)^bin);

assign borrow= ( ( a & b)| ( bin & ((a ^ b ))));

endmodule

**RTL Schematic**

FULL ADDER
![Screenshot 2025-04-22 223506](https://github.com/user-attachments/assets/a1a485de-1a7a-487a-8a45-b395e4d4eb5d)

FULL SUBTRACTOR
![Screenshot 2025-04-22 223653](https://github.com/user-attachments/assets/2158b732-53e8-42ad-bb4f-384a1e5a6354)

**Output Timing Waveform**
FULL ADDER
![Screenshot 2025-04-22 223749](https://github.com/user-attachments/assets/735ba1f2-1bc5-438d-89a7-09e8de74d453)

FULL SUBTRACTOR

![Screenshot 2025-04-22 223850](https://github.com/user-attachments/assets/f7d483b0-db15-4c15-85fa-ec53850ec902)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



