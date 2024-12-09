.# FULL_ADDER_SUBTRACTOR

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

![Screenshot 2024-12-07 161919](https://github.com/user-attachments/assets/f7933385-6247-4f2d-aa52-d6da7a1ad4d0)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![Screenshot 2024-12-07 163627](https://github.com/user-attachments/assets/3fd04439-93db-414d-b72f-866fc10104b2)

Borrow out = A'Bin + A'B + BBin

**Truthtable**
![Screenshot 2024-12-07 162645](https://github.com/user-attachments/assets/1a9fa0f1-bcb1-42cf-a49d-b57e5db7232a)


**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by:Reshma R RegisterNumber:2490406
```
(i)FULL ADDER
module fa(input a,b,c, output sum,carry);
wire w1,w2,w3;
assign sum=a^b^c;
assign w1=a&b;
assign w2=b&c;
assign w3=c&a;
assign carry=w1|w2|w3;
endmodule

(ii)FULL SUBTRACTOR
module fs(a,b,c,diff,borr);
input a,b,c;
output diff,borr;
wire w1,w2,w3,w4,w5,w6;
xor gi(diff,a,b,c);
and g2(w4,w1,b);
and g3(w5,w1,b);
and g4(w6,b,c);
or g5(borr,w4,w5,w6);
endmodule

**RTL Schematic**

**Output Timing Waveform**
![Screenshot 2024-12-07 162110](https://github.com/user-attachments/assets/038f2b71-d31f-4e3f-87eb-019708868052)
![Screenshot 2024-12-07 163803](https://github.com/user-attachments/assets/5175957a-b4fb-4a7f-9623-46248c10048f)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



