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


Full Adder

![image](https://github.com/AshwinKumar-Saveetha/FULL_ADDER_SUBTRACTOR/assets/155129814/e5e9b28c-8569-4f22-8d9a-f00f3791d592)


Full Subtractor

![image](https://github.com/AshwinKumar-Saveetha/FULL_ADDER_SUBTRACTOR/assets/155129814/a549746d-5b01-4493-af45-09d21f7b1b39)

**Procedure**

Full adder

1.Open Quartus II and create a new project.

2.Use schematic design entry to draw the full adder circuit.

3.The circuit consists of XOR, AND, and OR gates.

4.Compile the design, verify its functionality through simulation.

5.Implement the design on the target device and program it.

Full subtractor

1.Follow the same steps as for the full adder.

2.Draw the full subtractor circuit using schematic design.

3.The circuit includes XOR, AND, OR gates to perform subtraction.

4.Compile, simulate, implement, and program the design similarly to the full adder.

**Program:**

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by: TAMILPAGALAVAN

RegisterNumber: 2122223040224
```
module Fulladdsub(a,b,cin,sum,carry,BO,DIFF);
input a,b,cin;
output sum,carry,BO,DIFF;
assign sum=(a^b^cin);
assign carry=(a&b)|(a&cin)|(b&cin);
assign DIFF=(a^b^cin);
assign BO=(~a&b)|(~(a^b)& cin);
endmodule
```
**RTL Schematic**

![Screenshot 2024-03-19 143953](https://github.com/AshwinKumar-Saveetha/FULL_ADDER_SUBTRACTOR/assets/155129814/80d06b2e-6dbd-4f67-bf6b-d99f13b77d0c)

**Output Timing Waveform**
![Screenshot 2024-03-19 143850](https://github.com/AshwinKumar-Saveetha/FULL_ADDER_SUBTRACTOR/assets/155129814/0cc2e5bb-12b2-4593-a282-e444ee12875f)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



