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

module booleanmin(a,b,c,d,w,x,y,z,f1,f2);
input a,b,c,d,w,x,y,z;
output f1,f2;
wire adash,bdash,cdash,ddash,p,q,r,s,t,u;
not(adash,a);
not(bdash,b);
not(cdash,c);
not(ddash,d);
not(ydash,y);
and(p,bdash,ddash);
and(q,adash,b,d);
and(r,a,b,cdash);
or(f1,p,q,r);
and(s,ydash,z);
and(t,x,y);
and(u,w,y);
or(f2,s,t,u);
endmodule
 

Developed by:Iyalarasu C
RegisterNumber:212223040069



**RTL realization**

**Output:**

**RTL**
![image](https://github.com/Iyalarasu1/BOOLEAN_FUNCTION_MINIMIZATION/assets/144870581/f9be14a0-2454-4259-97d5-7fa06d3a4ec7)


**Timing Diagram**
![image](https://github.com/Iyalarasu1/BOOLEAN_FUNCTION_MINIMIZATION/assets/144870581/4169d42b-e70d-489e-87c0-2f402e8a038b)


**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

