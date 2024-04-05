# HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor

**Truthtable**

**Procedure**
```
1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.
```

**Program:**
```
/* Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by: Infancia Felcy P
 RegisterNumber: 212223040067
*/
Half Adder:
module exp3(sum, carry,a,b); 
input a,b; 
output sum,carry; 
xor sum1(sum,a,b); 
and carry1(carry,a,b); 
endmodule

Half Subractror:
module exp3(diff,carry,a,b);
input a,b;
output diff,carry;
xor(diff,a,b);
assign carry=(~a)&b;
endmodule

RTL schematic:
Half Adder:
![half adder](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/155411010/98e1ba28-1952-4263-9e53-947962f92b3e)
HAlf Subractor:
![half sub logic](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/155411010/f483e49b-601b-4989-b5a3-ebc09c56e50f)
Truth Table:
Half Adder:
![truth table half adder](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/155411010/f5c4dd99-d5e1-40f9-a25d-4df403185536)
Half Subractor:
![truth table half sub](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/155411010/a05a96e4-ffc1-42dd-846a-5bb46c3444a5)
Waveform:
Half Adder:
![3 logic wave form](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/155411010/2e2922e3-5b55-47c3-a10f-20c0b33d8fb2)
Half Subractor
![6317fa06-eb71-4449-b172-c5829e75db09](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/155411010/36ab959d-9322-4c8d-8265-d7d3c3b18170)

**Result:**Thus the half subtractor and half adder circuits are designed and the truth tables is verified using quartus software.
