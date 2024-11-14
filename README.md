#### NAME        : S.NAVINKUMAR
#### REG.NO      : 24901075
#### EXPERIMENT-3: HALF ADDER AND SUBTRACTOR
Implementation-of-Half-Adder-and-Half Subtractor-circuit

## AIM:

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

## EQUIPMENTS REQURIED:

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

## HALF ADDER:

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

## HALF SUBTRACTOR:

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor

## PROCEDURE:

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


## PROGRAM:
~~~~~~
module halfaddsub(a,b,sum,carry,difference,borrow);
input a,b;
output sum,carry,difference,borrow;
assign sum=a^b;
assign carry=a&b;
assign difference=a^b;
assign borrow=(~a)&b;
endmodule
~~~~~~~

## TRUTH TABLE:

![Screenshot 2024-11-08 094724](https://github.com/user-attachments/assets/c74401e4-5399-46bd-95a5-189073a08664)

![Screenshot 2024-11-08 094741](https://github.com/user-attachments/assets/8981b795-7d3d-4fc2-8df3-5a0aaa455df8)


## RTL OUTPUT:

![Screenshot 2024-11-08 093432](https://github.com/user-attachments/assets/1c137329-a473-4445-afb4-566ad755dd8e)


## OUTPUT WAVEFORM:

![Screenshot 2024-11-08 093555](https://github.com/user-attachments/assets/76496d18-d10b-4e8c-bcc9-e3809ed7c482)


## RESULT:

Designed a half adder and half subtractor circuit and verified its truth table in Quartus using Verilog programming.
