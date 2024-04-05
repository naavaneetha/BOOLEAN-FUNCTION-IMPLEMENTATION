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
RegisterNumber: 212223040067*/

HAlf Adder:
module exp3(sum, carry,a,b); 
input a,b; 
output sum,carry; 
xor sum1(sum,a,b); 
and carry1(carry,a,b); 
endmodule

Half Subractor:
module exp3(diff,carry,a,b);
input a,b;
output diff,carry;
xor(diff,a,b);
assign carry=(~a)&b;
endmodule


**RTL Schematic**
Half Adder:![51438f78-04e9-411e-b91f-b9c9350e798a](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/155411010/d8f48c2a-2e7e-434a-9af8-3cd94c591489)
Half Subractor:![c99c6a4a-8087-4d5c-bcec-a5bb41e292b3](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/155411010/2b401c1d-fee8-44ab-b0ca-9caf1354ae13)

Truth Table:
Half Adder:![f3ebcb6f-4a5a-4b4f-8186-94219a0d4117](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/155411010/54945479-325c-4822-a53a-5b70f746f1f2)

HALf Subractor:![6431d8f2-aafa-4d7c-87a8-e64a19e2522c](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/155411010/17f9bf82-b3f9-42fd-8ebf-ec11489d17d5)


Waveform:
HAlf Adder:![d28172aa-cec0-43f8-a4e2-39e117ed3e38](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/155411010/8659261c-27df-413f-a740-689fb680337b)
Half Suractor: ![6317fa06-eb71-4449-b172-c5829e75db09](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/155411010/05bf2ed4-7b3f-4b0f-b7f4-d7bb38655bfe)




**Output/TIMING Waveform**
```
**Result:**Thus the half subtractor and half adder circuits are designed and the truth tables is verified using quartus software.
