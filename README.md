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

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

FULL ADDER

![WhatsApp Image 2024-12-09 at 23 29 27_22987fe7](https://github.com/user-attachments/assets/bf06aae4-e8fe-4093-a3dc-ff1f436366d8)

FULL SUBTRACTOR

![WhatsApp Image 2024-12-09 at 23 29 28_9a53122b](https://github.com/user-attachments/assets/01551820-2a8d-4e7b-82aa-7c36cc56b3b4)

**Procedure**

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram

**Program:**

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by:shaiklahir

RegisterNumber:24005737

          module exp4(sum, cout, a, b, cin);
            output sum;
            output cout;
            input a;
            input b;
            input cin;
            wire s1, c1, c2;
            xor(s1,a,b);
            and(c1,a,b);
            xor (sum, s1, cin);
            and (c2, s1, cin);
            or (cout, c2, c1);
            endmodule
            
            module exp4a (df, bo, a, b, bin);
            output df;
            output bo;
            input a;
            input b;
            input bin;
            wire w1,w2, w3;
            assign w1=a^b;
            assign w2=(~a&b);
            assign w3=(~w1&bin);
            assign df=w1^bin;
            assign bo=w2/w3;
            endmodule


**RTL Schematic**

FULL ADDER

![Screenshot 2024-11-15 135804](https://github.com/user-attachments/assets/ff008e22-eea4-42e8-8c90-2f55cd548e13)

FULL SUBTRACTOR

![Screenshot 2024-11-15 140812](https://github.com/user-attachments/assets/e1b453ef-e589-4dac-a37b-d184ce8b5ee8)

**Timing Waveform**

FULL ADDER

![image](https://github.com/user-attachments/assets/6a171ee7-5789-40ce-b40f-702147f9c07c)


FULL SUBTRACTOR

![image](https://github.com/user-attachments/assets/530736ca-dab7-4f9c-aa25-8df81c1ce1ff)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



