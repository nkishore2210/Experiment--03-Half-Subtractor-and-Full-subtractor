# Experiment--03-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure



Write the detailed procedure here 


## Program:
/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: Kishore.N
RegisterNumber:  22008365
*/
HALF SUBTRACTOR:

module halfsub(A,B,Diff,Borrow);
input A,B; 
output Diff,borrow;
asssign Diff = (A ^ B);
assign Borrow = (~A & B);
endmodule
FULL SUBTRACTOR:

module fullsub(A,B,C,Diff,Borrow);
input A,B,C;
output Diff,Borrow;
assign Diff = (A^B^C);
assign borrow = (~a&(b^c)|(b&c));
endmodule 

## Output:

Half subtractor:

RTL:
![image](https://user-images.githubusercontent.com/118707090/214312530-2ef090aa-1343-407a-a449-72253715af0d.png)
Truth Table:
![image](https://user-images.githubusercontent.com/118707090/214312621-cc621ee4-f464-41bf-861a-8aa8394bf121.png)
Waveform:
![image](https://user-images.githubusercontent.com/118707090/214312722-9a11249a-f557-408c-b2b8-115fef54698c.png)

Full subtractor:

RTL:
![image](https://user-images.githubusercontent.com/118707090/214312785-fe120e5d-8a0e-4a71-b190-f3268aef94ad.png)
Truth Table:
![image](https://user-images.githubusercontent.com/118707090/214313095-5b5b6e69-c7da-4e3e-98eb-31820269ec16.png)
Waveform:
![image](https://user-images.githubusercontent.com/118707090/214313164-ee1a65a8-81b9-4b66-b227-4db1ea5e2152.png)



## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
