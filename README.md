# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

 Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 
```
module Boolean_min(a,b,c,d,w,x,y,z,f1,f2);
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
not(ydash,y);
and(s,ydash,z);
and(t,x,y);
and(u,w,y);
or(f2,s,t,u);
endmodule

Developed by :VIJAY R
RegisterNumber:212223240022

```
![WhatsApp Image 2024-03-22 at 13 50 29_c317f4e9](https://github.com/vijayr21/BOOLEAN_FUNCTION_MINIMIZATION/assets/149347607/b9e61c32-114d-4376-a386-91457b1d63a7)

![WhatsApp Image 2024-03-22 at 13 50 30_2ce4d203](https://github.com/vijayr21/BOOLEAN_FUNCTION_MINIMIZATION/assets/149347607/770f3ae3-8b30-4d65-a148-c6b296a23b65)



**Output:**
 ![alt text](<Screenshot 2024-03-15 141340.png>)

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

