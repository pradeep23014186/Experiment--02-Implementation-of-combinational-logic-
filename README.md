# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
 
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime


## Theory
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.
 

## Logic Diagram (using nand gate) and (using nor gate):
![image](https://github.com/pradeep23014186/Experiment--02-Implementation-of-combinational-logic-/assets/152294642/91bba5d6-e0b9-4948-92a7-f71b015e9f21)
![image](https://github.com/pradeep23014186/Experiment--02-Implementation-of-combinational-logic-/assets/152294642/5e2f031b-7bfc-476b-9dea-536e2d54380a)

## Procedure
*Create a project with required entities.

*Create a module along with respective file name.

*Run the respective programs for the given boolean equations.

*Run the module and get the respective RTL outputs.

*Create university program(VWF) for getting timing diagram.

*Give the respective inputs for timing diagram and obtain the results.

## Program:
```
Developed by: Pradeep Kumar.G
RegisterNumber: 23014186
```
```
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
module combinational(a,b,c,d,w,x,y,z,fl,f2);
input a,b,c,d,w,x,y,z;
output fl,f2;
wire g1=((~a)&(~b)&(~c)&(~d)); 
wire g2=((a)&(~c)&(~d));
wire g3=((~b)&(c)&(~d));
wire g4=((~a)&(b)&(c)&(d)); 
wire g5=((b)&(~c)&(d));
assign fl=g1|g2|g3|g4|g5; 
wire g6=((x)&(~y)&(z));
wire g7=((~x)&(~y)&(z));
wire g8=((~w)&(x)&(y)); 
wire g9=((w)&(~x)&(y));
wire g10=((w)&(x)&(y)); 
assign f2=g6|g7|g8|g9|g10;
endmodule
```

## Output:
## RTL realization of NAND AND NOR gates:
![image](https://github.com/pradeep23014186/Experiment--02-Implementation-of-combinational-logic-/assets/152294642/19e725e9-58ef-4a75-b89c-4012afb41141)
## Truthtable of NAND gate:
![image](https://github.com/pradeep23014186/Experiment--02-Implementation-of-combinational-logic-/assets/152294642/50f81e24-9672-4f4b-b009-fafda9aab4cf)
## Truthtable of NOR gate:
![image](https://github.com/pradeep23014186/Experiment--02-Implementation-of-combinational-logic-/assets/152294642/9656f460-2bbd-4812-a2f0-23042750441f)

## Timing Diagram:
![image](https://github.com/pradeep23014186/Experiment--02-Implementation-of-combinational-logic-/assets/152294642/0e1522e0-4977-4696-91ea-d6d878b0a85a)

## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
