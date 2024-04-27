# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

**Logic Diagram**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 

Developed by: Sriram R
RegisterNumber:212223230215
```
module BMf1f2(a,b,c,d,w,x,y,z,f1,f2);
  input a,b,c,d,w,x,y,z;
  output f1,f2;
wire adash,bdash,cdash,ddash,ydash,p,q,r,s,t,u;
  not(adash,a);
  not(bdash,b);
  not(cdash,c);
  not(ddash,d);
  and(p,bdash,ddash);
  and(q,adash,b,d);
  and(r,a,b,cdash);
  or(f1,p,q,r);
//type code for f2 as like f1
 not(ydash,y);
 and(s,x,y);
 and(t,ydash,z);
 and(u,w,y);
 or(f2,s,t,u);
endmodule
```

## RTL realization
![image](https://github.com/Rsriram13/BOOLEAN_FUNCTION_MINIMIZATION/assets/145742823/6b984a74-5836-44d8-a927-73e49f4dcc1e)

## Timing Diagram
![image](https://github.com/Rsriram13/BOOLEAN_FUNCTION_MINIMIZATION/assets/145742823/e8ad3dff-3f67-4ff7-8372-9f0ccb4167ff)
## Result:

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

