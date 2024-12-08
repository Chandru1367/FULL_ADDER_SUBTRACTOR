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

**Procedure**
```
1)Open Quartus2
2)open new file
3)create veri log file and using tools view the logic diagram
4)Then click on netlist viewer and press RTL viewer to view the OUTPUT in graph format
```
**Program:**

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

```
1)FULL ADDER
module fulladder(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule
```
```
2)FULL SUBRACTOR
module fs(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( a & b)| ( bin & ((a ^ b ))));
endmodule
```
Developed by: M.Chandru

RegisterNumber: 24900224

**RTL Schematic**
 
 1)FULL ADDER
 
<img width="466" alt="image" src="https://github.com/user-attachments/assets/b398b5ce-480f-4bdb-ae64-089fd9d6aa24">

2)FULL SUBRACTOR

<img width="616" alt="image" src="https://github.com/user-attachments/assets/5419fc0a-30a4-4f40-9325-04d44fd3bc5d">

**Output Timing Waveform**

1)FULL ADDER

<img width="755" alt="image" src="https://github.com/user-attachments/assets/3eaa0b1e-6239-4bab-9173-fc7f4cd3ca84">


2)FULL SUBRACTOR

<img width="722" alt="image" src="https://github.com/user-attachments/assets/107eecf2-bada-48be-8692-cce251c7bb7f">


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



