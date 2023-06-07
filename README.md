# Experiment--04-Half-Subtractor-and-Full-subtractor
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

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: NIVETHA K 
RegisterNumber:212222230102


HALF SUBTRACTOR
```
module HalfSubtractor(A,B,Diff,Borrow);
input A,B;
output Diff,Borrow;
wire x;
xor (Diff, A,B);
not(x,A);
and(Borrow,x,B);
endmodule
```

Full subtractor:
```
module FullSubtractor(A,B,C,Diff,Borrow);
input A,B,C;
output Diff,Borrow;
wire p;
assign Diff = ((A^B)^C);
not(p,A);
assign Borrow = ((p&B)|(p&C)|(B&C));
endmodule
```
## Output:

Half subtractor gates :

![1](https://github.com/NivethaKumar30/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119559844/56baf22e-8051-43e5-98a9-4b7131da93be)

Truthtable

![2](https://github.com/NivethaKumar30/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119559844/71db73ae-58f0-4275-8bda-34d5ed73c818)

RTL realization

![3](https://github.com/NivethaKumar30/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119559844/0c0d2cd4-fb01-470d-bf93-773f3eb4f542)

Timing diagram

![4](https://github.com/NivethaKumar30/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119559844/d70ad0fb-36bb-4aa2-b5d6-1eccdee4e142)

Full Subractor: Gates:

![5](https://github.com/NivethaKumar30/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119559844/306dfaaf-d1f8-430f-8d5e-225345055a8c)

Truthtable :

![6](https://github.com/NivethaKumar30/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119559844/d1fc1c23-fbcf-487b-9fc1-8b1db2ace334)

Truthtable :

![7](https://github.com/NivethaKumar30/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119559844/b6805c2d-aba9-4102-a4c5-f0888f6a1255)

Timing diagram :

![8](https://github.com/NivethaKumar30/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119559844/f05c0985-8425-4e5f-8d64-d9e5a89d7736)




## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
