# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

![Screenshot 2025-04-23 230658](https://github.com/user-attachments/assets/edf92575-ea99-4d5e-a67f-07d61e1c5237)


**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

![Screenshot 2025-04-23 230831](https://github.com/user-attachments/assets/61507927-ce32-4e7d-a2d3-468024d86912)


**Truthtable**
Full adder
![Screenshot 2025-04-23 230930](https://github.com/user-attachments/assets/8eb552a5-01a4-40b0-9703-de92fd242f93)
Full subractor
![Screenshot 2025-04-23 231012](https://github.com/user-attachments/assets/12d3ee0a-2aca-444f-832d-96dd8cbd0a89)


**Procedure**

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.


**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by:S.Suruthi
RegisterNumber:212224220114
```
Full adder

//full adder
module exp4(sum,cout,a,b,cin);
output sum;
output cout;
input a;
input b;
input cin;

//internal nets
wire s1,c1,c2;


//instantiate logic gate primitives
xor (s1,a,b);
and (c1,a,b);
xor(sum,s1,cin);
and(c2,s1,cin);
or(cout,c2,c1);


endmodule

Full subtractor

module exp4a (df,bo,a,b,bin);
output df;
output bo;
input a;
input b;
input bin;
wire w1,w2,w3;
assign w1=a^b;
assign w2=(~a&b);
assign w3=(~w1&bin);
assign df=^bin;
assign bo=w2|w3;
endmodule
```

**RTL Schematic**
Full adder

![Screenshot 2025-04-23 231357](https://github.com/user-attachments/assets/ea5dd6ac-2175-4083-8a43-023672ca8577)

Full subractor

![Screenshot 2025-04-23 231510](https://github.com/user-attachments/assets/bc7b26d7-53a3-40ae-a0a9-92708126ab52)



**Output Timing Waveform**
Full adder

![Screenshot 2025-04-23 232238](https://github.com/user-attachments/assets/d1f0dcbc-52c7-4dfb-bb58-1a7e1641289f)


Full subractor

![Screenshot 2025-04-23 231713](https://github.com/user-attachments/assets/b94e9fda-8ee7-448f-b56f-4910a31ded2e)




**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



