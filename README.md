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



**Full Adder:**



![image](https://github.com/dhivyadharshini2006/FULL_ADDER_SUBTRACTOR/assets/144979490/d0bba8f3-9dbd-4d97-b357-71daf645f363)



**Full Subtractor:**


![image](https://github.com/dhivyadharshini2006/FULL_ADDER_SUBTRACTOR/assets/144979490/095e9946-52b2-46bd-b46e-130ced85eb8f)


**Procedure**

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.

**Program:**
```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by:Dhivya Dharshini B
RegisterNumber:212223240031

Full Adder:
module ff(a,b,cin,sum,carry);
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

Full Subtractor:
module fa(a,b,Bin,BO,DIFF);
input a,b,Bin;
output BO,DIFF;
assign DIFF = a ^ b ^ Bin;
  assign BO = (a & b) | ((a ^ b) & Bin);
endmodule



```
**RTL Schematic**




**Full Adder:**


![Screenshot 2024-03-23 203917](https://github.com/dhivyadharshini2006/FULL_ADDER_SUBTRACTOR/assets/144979490/1893145e-1285-438d-883e-d521fa4e0bfd)


**Full Subtractor:**




![image](https://github.com/dhivyadharshini2006/FULL_ADDER_SUBTRACTOR/assets/144979490/05b6dcd5-cbe5-4b5f-a8a9-3a69090a97d4)


**Output Timing Waveform**






**Full Adder:**



![image](https://github.com/dhivyadharshini2006/FULL_ADDER_SUBTRACTOR/assets/144979490/6d65dde2-1573-48c9-ad18-02ec5f1e7935)



**Full Subtractor:**


![image](https://github.com/dhivyadharshini2006/FULL_ADDER_SUBTRACTOR/assets/144979490/baefd6fe-33ff-47cb-9d4a-2d26a8213782)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



