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
![WhatsApp Image 2024-12-09 at 09 06 05_07f05334](https://github.com/user-attachments/assets/985fdf4c-fb8b-4a23-872f-d0baa040e6fc)


**Truthtable**
![WhatsApp Image 2024-12-09 at 09 06 05_a10eb4cb](https://github.com/user-attachments/assets/ce4c322e-e855-4f97-9205-e84558efcad8)


**Procedure**
1) type the program in quartus software
2) complete and run the program
3) generate the RTL schematic and save the logic diagram
4) Create nodes for inputs and outputs to generate the timing diagram
5) for different input combinations generate the timing diagram
   

**Program:**
FULL ADDER

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
assign borrow= ( ( a & b)| ( bin & ((a ^ b ))));
endmodule

**RTL Schematic**
![4 rtl 1](https://github.com/user-attachments/assets/6ab16dd4-d36f-488a-b5a2-3a368bb4c12b)
![4 rtl 2](https://github.com/user-attachments/assets/87f17fa9-23ca-48b8-92ae-75a32a634709)




**Output Timing Waveform**
![4 td 1](https://github.com/user-attachments/assets/4c80523f-3a69-4aa3-8cd3-c3f22652aa95)

![4 td 2](https://github.com/user-attachments/assets/9a532e99-2b3d-4457-ad64-438a1e76ff34)




**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



