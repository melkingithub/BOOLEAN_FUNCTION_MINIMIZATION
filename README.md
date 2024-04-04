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
````
Developed by: MELKIN SAM. D RegisterNumber:212223220056*/
//Program to compute the function f1=a'b'c'd'+ac'd'+b'cd'+a'bcd+bc'd
//f2=xy'z+x'y'z+w'xy+wx'y+wxy
// simplify the logic using Boolean minimization/k map 
//compute f2 and write verilog code for f2 as like f1
module boolean_function(a,b,c,d,w,x,y,z,f1,f2);
input a,b,c,d,w,x,y,z;
output f1,f2;
wire adash,bdash,cdash,ddash,ydash,p,q,r,s,t,u;
not(adash,a);
not(bdash,b);
not(cdash,c);
not(ddash,d);
not(ydash,y);
and(p,bdash,ddash);
and(q,adash,b,d);
and(r,a,b,cdash);
or(f1,p,q,r);
//type code for f2 as like f1
and(s,ydash,y);
and(t,x,y);
and(u,w,y);
or(f2,s,t,u);
endmodule
`````
**RTL realization**

**Output:**
![image](https://github.com/23006823/BOOLEAN_FUNCTION_MINIMIZATION/assets/138971409/234420c8-a531-4214-aa6f-a0f3f5f519fd)


**RTL**
**Timing Diagram**
![image](https://github.com/23006823/BOOLEAN_FUNCTION_MINIMIZATION/assets/138971409/f4811600-0c0f-4414-bf8b-7037c2ad1831)

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.
