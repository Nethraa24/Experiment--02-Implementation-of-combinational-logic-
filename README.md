# Experiment--02-Implementation-of-combinational-logic
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.

 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
 
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime


## Theory
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.
 

## Program:
/*
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.

Developed by: J NETHRAA

RegisterNumber: 212222100031
*/
```python
module Verilog1(a,b,c,d,w,x,y,z,F1,F2);
input a,b,c,d,w,x,y,z;
output F1,F2;
wire  A1,A2,A3,A4,A5,B1,B2,B3,B4,B5;
assign A1= (~a&(~b)&(~c)&(~d));
assign A2= (a&c&(~d));
assign A3= ((~b)&c&(~d));
assign A4= (~a&b&c&d);
assign A5= (b&(~c)&d);
assign F1= A1|A2|A3|A4|A5;
assign B1= (x&(~y)&z);
assign B2= (~x&(~y)&z);
assign B3= (~w&x&y);
assign B4= (w&(~x)&y);
assign B5= (w&y&z);
assign F2= B1|B2|B3|B4|B5;
endmodule		 
```
## Output:
## RTL
![image](https://user-images.githubusercontent.com/118343401/234772584-e3313e30-289d-4b70-9ef6-f248462c4cf8.png)

## Timing Diagram
![image](https://user-images.githubusercontent.com/118343401/234772642-539c32b6-4dec-4993-92a5-002c09487a2f.png)

## Truth table
![image](https://user-images.githubusercontent.com/118343401/234773724-b57a84a0-a38f-4533-92f6-2e6893e5513e.png)

## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
