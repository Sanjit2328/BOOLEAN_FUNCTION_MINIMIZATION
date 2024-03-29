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

Developed by: Sanjit.P

RegisterNumber: 212223230190
~~~

//Program to compute the function f1=a'b'c'd'+ac'd'+b'cd'+a'bcd+bc'd
//f2=xy'z+x'y'z+w'xy+wx'y+wxy
// simplify the logic using Boolean minimization/k map 
//compute f2 and write verilog code for f2 as like f1
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

~~~

![Screenshot 2024-03-21 094816](https://github.com/Meenu2823/BOOLEAN_FUNCTION_MINIMIZATION/assets/139416219/6d15f315-f552-4271-84cc-c88ea2047317)

**RTL realization**

![Screenshot 2024-03-21 092618](https://github.com/Meenu2823/BOOLEAN_FUNCTION_MINIMIZATION/assets/139416219/de44cdf3-076c-42a4-aa29-a6ac23ee33b3)

**Output:**

![Screenshot 2024-03-21 094514](https://github.com/Meenu2823/BOOLEAN_FUNCTION_MINIMIZATION/assets/139416219/8d171afc-ba93-4ca8-a618-7a115f25cbe4)

**Result:**

Thus,the given logic functions are implemented using and their operations are verified using Verilog programming.

