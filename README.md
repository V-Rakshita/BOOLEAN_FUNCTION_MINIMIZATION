### Name: V Rakshita
### Reg no: 212224100049

# EXP 2 - BOOLEAN FUNCTION

## **AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

## **Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

## **Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


## **Program:**
```
module EXP2(a,b,c,d,w,x,y,z,f1,f2);
input a,b,c,d,w,x,y,z;
output f1,f2;
wire x1,x2,x3,x4,y1,y2,y3,y4,y5;
assign x1=((~a)&(~b)&(~c)&(~d));
assign x2=(a&(~c)&(~d));
assign x3=((~b)&(c)&(~d));
assign x4=((~a)&(b)&(c)&(d));
assign x5=(b&(~c)&(d));
assign f1=x1|x2|x3|x4|x5;

assign y1=(x&(~y)&(z));
assign y2=((~x)&(~y)&z);
assign y3=((~w)&x&y);
assign y4=(w&(~x)&y);
assign y5=(w&x&y);
assign f2=y1|y2|y3|y4|y5;
endmodule
```

## **Truth Table and Logic Diagram:**

![Screenshot (222)](https://github.com/user-attachments/assets/fa616d02-fd72-46e4-a314-fe1ba7b46f08)

![Screenshot (223)](https://github.com/user-attachments/assets/ab7d39df-e6b8-4a1c-bed9-56b96ae970fd)

![Screenshot (217)](https://github.com/user-attachments/assets/9c74e086-d655-448f-9716-140a4e4b2880)

## **Waveform:**

![WhatsApp Image 2025-04-15 at 21 38 27_13e76a24](https://github.com/user-attachments/assets/0de4bf30-b862-4377-8e83-61be9b68d9ea)


## **Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

