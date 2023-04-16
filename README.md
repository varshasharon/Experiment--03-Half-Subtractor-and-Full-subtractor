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
1.Use module project name(input,output) to start the Verilog programmming.

2.Assign inputs and outputs using the word input and output respectively.

3.Use defined keywords like wire,assign and required logic gates to represent the boolean expression.

4.Use each output to represent one for difference and the other for borrow.

5.End the verilog program using keyword endmodule.


## Program:
```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: E. VARSHA SHARON
RegisterNumber:  212222100058

HALF SUBTRACTOR

module HS(a,b,d,bo);
input a,b;
output d,bo;
assign d = (a^b);
assign bo = (~a&b);
endmodule

FULL SUBTRACTOR

module FS(A,B,C,Difference,Borrow);
input A,B,C;
output Difference,Borrow;
assign Difference = (A^B^C);
assign Borrow = (~A&(B^C)|(B&C));
endmodule
```

## Output:

## Truthtable
HALF SUBTRACTOR
![image](https://user-images.githubusercontent.com/98278161/232317425-3b6c24b8-34e7-4837-9a88-daf0c3ba2ed1.png)

FULL SUBTRACTOR
![image](https://user-images.githubusercontent.com/98278161/232317532-e3ba133f-7101-46e7-9160-484704120976.png)




##  RTL realization
HALF SUBTRACTOR
![image](https://user-images.githubusercontent.com/98278161/232317693-ef82bbfc-ab30-4ba0-a63d-4631674e03a9.png)
FULL SUBTRACTOR
![image](https://user-images.githubusercontent.com/98278161/232317805-c8c8d61f-d25d-40a8-8666-071b646b6756.png)


## Timing diagram 
HALF SUBTRACTOR
![image](https://user-images.githubusercontent.com/98278161/232317935-d19adf7a-badc-49d8-ad88-87e7026cbb08.png)
FULL SUBTRACTOR
![image](https://user-images.githubusercontent.com/98278161/232318004-e0b40d4e-52cf-4edb-8157-f6ee2acd198c.png)

## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
