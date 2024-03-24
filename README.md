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

 Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 

**Developed by:NISHA.D**

**RegisterNumber:212223230143**
```
//Program to compute the function f1=a'b'c'd'+ac'd'+b'cd'+a'bcd+bc'd
//f2=xy'z+x'y'z+w'xy+wx'y+wxy
// simplify the logic using Boolean minimization/k map 
//compute f2 and write verilog code for f2 as like f1
module BM(a,b,c,d,w,x,y,z,f1,f2);
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
//type code for f2 as like f1
not(ydash,y);
and(s,x,y);
and(t,ydash,z);
and(u,w,y);
or(f2,s,t,u);
endmodule

```

![Screenshot (139)](https://github.com/Nishadayalan/BOOLEAN_FUNCTION_MINIMIZATION/assets/144870468/f5936d79-1e9e-4037-98f1-7c453afa28fb)




**RTL realization**

**Truth Table:**

![image](https://github.com/keerthanapillaram/BOOLEAN_FUNCTION_MINIMIZATION/assets/145743072/89b083e7-5dbd-47c4-851a-6adf4d83bc46)

**RTL:**

![Screenshot (140)](https://github.com/Nishadayalan/BOOLEAN_FUNCTION_MINIMIZATION/assets/144870468/0081e19e-f2c3-4a0c-b39a-09150f8fa39a)


**Timing Diagram:**

![Screenshot (141)](https://github.com/Nishadayalan/BOOLEAN_FUNCTION_MINIMIZATION/assets/144870468/0edca49c-4e21-4fb0-b0db-58ddc6710fe5)

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

