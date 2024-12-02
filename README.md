Full-subtractor-circuit

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

Borrow out = A'Bin + A'B + BB
**Procedure**

A full subtractor is a combinational logic circuit that performs subtraction of three binary digits (minuend, subtrahend, and borrow-in). It takes into account the borrow from the previous lower significant bit. The output consists of two bits: Difference (D) and Borrow-out (B_out).
Write the detailed procedure here

**Program:**
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

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by:Vishvanandh N

RegisterNumber:24005857
*/

**RTL Schematic**
![WhatsApp Image 2024-12-02 at 21 14 11_8c1ad90d](https://github.com/user-attachments/assets/30830055-5f1f-4321-b0a1-eec9883b9acf)![WhatsApp Image 2024-12-02 at 21 14 11_15ae1f09](https://github.com/user-attachments/assets/d4cbfbd5-cb88-4665-8b25-46bbbc35ad0e)


**Output Timing Waveform**
![WhatsApp Image 2024-12-02 at 21 14 11_220b09eb](https://github.com/user-attachments/assets/f2706558-7336-4346-8a29-636920c490c6)![WhatsApp Image 2024-12-02 at 21 14 11_caaede12](https://github.com/user-attachments/assets/4d4f1a81-9518-4510-aba8-a20de44d0050)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



