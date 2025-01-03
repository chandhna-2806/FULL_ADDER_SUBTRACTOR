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
![WhatsApp Image 2024-12-08 at 20 04 44_07ab69b0](https://github.com/user-attachments/assets/d5860981-0cbf-44d9-a8af-995e27cc11f7)
![WhatsApp Image 2024-12-08 at 20 05 50_6c1748ab](https://github.com/user-attachments/assets/7abdb9d4-f6fe-4343-befc-01757386e620)



**Output Timing Waveform**
![WhatsApp Image 2024-12-08 at 20 05 14_a3ca6ebf](https://github.com/user-attachments/assets/279558ae-db25-4498-b0e2-55749af1ceeb)
![WhatsApp Image 2024-12-08 at 20 07 09_afc69ac8](https://github.com/user-attachments/assets/c444368b-5064-4b5f-80cd-fe60fe0fa6bd)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



