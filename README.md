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

**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/

FULL_ADDER:
'''
module full_adder(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
wire w1,w2,w3,w4;       
xor(w1,a,b);
xor(sum,w1,cin);        

and(w2,a,b);
and(w3,b,cin);
and(w4,cin,a);

or(carry,w2,w3,w4);
endmodule
'''
FULL_SUBRACTOR:
'''
module full_subtracter(a,b,Bin,BO,DIFF);
input a,b,Bin;
output BO,DIFF;
assign DIFF = a ^ b ^ Bin;
  assign BO = (a & b) | ((a ^ b) & Bin);
endmodule

'''
DEVELOPED BY:VESLIN ANISH
REGISTER NO:212223240175

**RTL Schematic**
FULL_ADDER:
![WhatsApp Image 2024-04-03 at 08 00 14_e86ce16e](https://github.com/veslin23000303/FULL_ADDER_SUBTRACTOR/assets/151148539/ebadfbf8-c469-4197-8bf3-a0492548419e)

FULL_SUBTRACTOR:
![WhatsApp Image 2024-04-03 at 08 00 41_9ac13625](https://github.com/veslin23000303/FULL_ADDER_SUBTRACTOR/assets/151148539/30b8c910-7fa2-46ac-bd1e-1d5e40e5f3d4)




**Output Timing Waveform**
FULL_ADDER:
![WhatsApp Image 2024-04-03 at 08 00 55_2a02cb4b](https://github.com/veslin23000303/FULL_ADDER_SUBTRACTOR/assets/151148539/acbe3cd0-7a92-4e1b-8fa8-57e6294a5ff0)


FULL_SUBTRACTOR:
![WhatsApp Image 2024-04-03 at 08 01 11_945997d7](https://github.com/veslin23000303/FULL_ADDER_SUBTRACTOR/assets/151148539/88b9a2eb-6db1-4c25-b24d-7c98323bbd41)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



