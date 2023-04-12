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

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: NIVETHA K 
RegisterNumber:212222230102

```
Half subtractor:
module halfsub(output B,D, input X,Y); 

assign D = (X ^ Y); 

assign B = (~X & Y);

endmodule
```
```
Full subtractor:
module fullsub(X,Y,Z,Borrow,Difference); 

input X,Y,Z; 

output Borrow,Difference; 

assign Difference = (X^Y^Z); 

assign Borrow = (~X&(Y^Z)|(Y&Z)); 

endmodule
```
## Output:

Half subtractor:


RTL realization

![RTL 1 ](https://user-images.githubusercontent.com/119559844/231472143-3ef6da33-0119-4000-a1d2-9dd21fba3716.png)

## Timing diagram 

![TIMING ](https://user-images.githubusercontent.com/119559844/231472344-9a30452f-15a4-4e0a-a945-8cf81041340b.png)

## Truthtable

![TT4 ](https://user-images.githubusercontent.com/119559844/231472699-04896f0b-efa7-44fc-866a-0ad73a2df746.png)

Full subtractor:

##  RTL realization

![f](https://user-images.githubusercontent.com/119559844/231475182-fed2a7d8-7fa7-4f4c-802e-ce1bf77a73d3.png)

## Timing diagram 

![c](https://user-images.githubusercontent.com/119559844/231474992-050c04d6-87b7-4e67-a7e3-ef1fc45a7922.png)

## Truthtable

![k](https://user-images.githubusercontent.com/119559844/231475035-1c8aaef8-ee33-42b7-b8ef-3401b06a63da.png)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
