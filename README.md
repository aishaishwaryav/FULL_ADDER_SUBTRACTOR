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
![image](https://github.com/aishaishwaryav/FULL_ADDER_SUBTRACTOR/assets/151565589/eb786c44-9b39-4f1d-8273-a820dfbb5c2f)

FULL SUBTRACTOR
![image](https://github.com/aishaishwaryav/FULL_ADDER_SUBTRACTOR/assets/151565589/c22aa48a-2041-43d3-859b-37a6d6680e11)

**Procedure**

Write the detailed procedure here
```
STEP-1 Open Quartus Prime software.

STEP-2 Create a new project and select the target FPGA device.

STEP-3 Design and implement the full adder/subtractor using Verilog or VHDL within a new HDL file.

STEP-4 Add the HDL file to the project and compile the design.

STEP-5 Program the FPGA with the compiled design to test the functionality of the full adder/subtractor.
```

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/
```
module fulladdsub(a,b,c,sum,carry,BO,DIFF);
input a,b,c;
output sum,carry,BO,DIFF;
assign sum=a^b^c;
assign carry= a&b | a&c | b&c;
wire a0;
not (a0,a);
assign BO= b&c | a0&c | a0&b;
assign DIFF=a^b^c;
endmodule

Developed by: AISHWARYA V
RegisterNumber: 212223220003
```

**RTL Schematic**

![image](https://github.com/aishaishwaryav/FULL_ADDER_SUBTRACTOR/assets/151565589/3d983108-fc52-4710-888e-8274ea3a5efc)


**Output Timing Waveform**
FULL ADDER

![image](https://github.com/aishaishwaryav/FULL_ADDER_SUBTRACTOR/assets/151565589/5432f2be-76aa-4fd7-a708-d91794f3ced9)

FULL SUBTRACTOR
![image](https://github.com/aishaishwaryav/FULL_ADDER_SUBTRACTOR/assets/151565589/415b2781-629b-47e7-86e0-d197ed566a20)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



