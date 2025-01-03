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

![Screenshot 2025-01-02 200923](https://github.com/user-attachments/assets/185a639b-aa1b-497d-8140-bcdf358c4306)

![Screenshot 2025-01-02 201003](https://github.com/user-attachments/assets/387b4626-3b4e-476c-a716-0783404571d2)



**Procedure**

type the program in quartes software.

2 compile and run rhe program .

3 generate the RTL schematic and save the logic diagram.

4 create nodes for inputs and outputs to generate the timing diagram .

5 for different input combinations generate the timing diagram
**Program:**
FULL ADDER

module fulladder(

input a,b,c,

output sum,carry);

wire w1,w2,w3;

assign sum=a^b^c; assign w1=a&b;

assign w2=b&c;

assign w3=c&a;

assign carry=w1|w2|w3;

endmodule

FULL SUBRACTOR

module fullsub(a,b,c,diff,borr);

input a,b,c;

output diff,borr;

wire w1,w2,w3,w4,w5,w6;

xor g1(diff,a,b,c);

and g2(w4,w1,b);

and g3(w5,w1,b);

nd g4(w6,b,c);

or g5(borr,w4,w5,w6);

endmodule

Developed by:R.mounish vamsi kumar 

RegisterNumber:24003774
*/

**RTL Schematic**

FULL ADDER

![Screenshot 2025-01-02 200413](https://github.com/user-attachments/assets/0b184bf4-37a9-4e00-a94d-d3497fbb5b12)

FULL SUBTRACTOR

![Screenshot 2025-01-02 200450](https://github.com/user-attachments/assets/0d074628-a86a-466f-ae0f-79b76e5844ac)


**Output Timing Waveform**

FULL ADDER

![Screenshot 2025-01-02 200137](https://github.com/user-attachments/assets/5bc5008f-16cb-4101-ade4-d466979be2ac)

FULL SUBTRACTOR


![Screenshot 2025-01-02 200210](https://github.com/user-attachments/assets/6816803f-8ada-4b20-a30c-230e404c6a13)




**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



