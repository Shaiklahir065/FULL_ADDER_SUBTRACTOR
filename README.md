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
![WhatsApp Image 2024-12-09 at 23 29 27_22987fe7](https://github.com/user-attachments/assets/bf06aae4-e8fe-4093-a3dc-ff1f436366d8)

![WhatsApp Image 2024-12-09 at 23 29 28_9a53122b](https://github.com/user-attachments/assets/01551820-2a8d-4e7b-82aa-7c36cc56b3b4)

**Procedure**

Write the detailed procedure here

**Program:**

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by:shaiklahir RegisterNumber:24005737

          i)FULL ADDER
          
          module fa(a,b,cin,sum,carry);
          input a,b,cin;
          output sum,carry;
          assign sum=( (a ^ b)^cin);
          assign carry= ( (a & b)| ( cin &(a ^ b )));
          endmodule

    ii)FULL SUBTRACTOR
    
    module fs(a,b,bin,difference,borrow);
    input a,b,bin;
    output difference,borrow;
    assign difference= ( (a ^ b)^bin);
    assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
    endmodule


**RTL Schematic**
![Screenshot 2024-11-15 135804](https://github.com/user-attachments/assets/ff008e22-eea4-42e8-8c90-2f55cd548e13)
![Screenshot 2024-11-15 140812](https://github.com/user-attachments/assets/e1b453ef-e589-4dac-a37b-d184ce8b5ee8)

**Timing Waveform**
![min_fa](https://github.com/user-attachments/assets/2da1e502-6a55-4692-b3f4-f18343f8650c)
![min_fs](https://github.com/user-attachments/assets/a5d363b7-121f-4e12-b30d-09980c62594a)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



