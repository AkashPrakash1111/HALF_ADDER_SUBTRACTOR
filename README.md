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
![Screenshot 2024-11-16 204607](https://github.com/user-attachments/assets/d1e84b23-0b43-495f-a276-e9c1aba4f692)


Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B
![Screenshot 2024-11-16 211034](https://github.com/user-attachments/assets/483b9a58-bbdd-4143-948f-4fddbb992c8a)


Figure -02 HALF Subtractor

**Truthtable**

a	b	sum (a ^ b)	carry (a & b)
0	0	0	0
0	1	1	0
1	0	1	0
1	1	0	1
![image](https://github.com/user-attachments/assets/323de566-3a1f-473d-923e-210e1c1e559e)

a	b	difference (a ⊕ b)	borrow (~a & b)
0	0	0	0
0	1	1	1
1	0	1	0
1	1	0	0
![image](https://github.com/user-attachments/assets/3690a9ac-0f34-4201-9b45-c77ff9e07059)

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

module halfadder(a,b,sum,carry);


input a,b;


output sum,carry;


assign sum= (a ^ b);


assign carry= ( a & b);


endmodule


i)Halfsubtractor:

module hs(a,b,difference,borrow);


input a,b;


output difference,borrow;


assign difference= (a ^ b);


assign borrow= ( ~a & b);


endmodule



/* Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by: RegisterNumber:*/

**RTL Schematic**
![Screenshot 2024-11-16 204932](https://github.com/user-attachments/assets/5208d949-2092-4e0b-81e6-f9785c9aff1e)

![Screenshot 2024-11-16 211303](https://github.com/user-attachments/assets/60d2f7f5-60c0-4db8-9111-9a4ce5f9187e)

**Output/TIMING Waveform**

**Result:**
Thus the given half adder and  half subtractor fuctions are implemented and their operators are verified using Verilog programming.
