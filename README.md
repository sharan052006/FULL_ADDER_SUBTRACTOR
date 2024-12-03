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
![WhatsApp Image 2024-12-02 at 21 33 48_0482fe98](https://github.com/user-attachments/assets/c42fe750-05ed-4bb4-ac67-ab34e3795bb3)


**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
```
full adder:
module fulladder(a, b, cin, sum, carry); 
    input a; 
    input b; 
    input cin; 
    output sum; 
    output carry; 
 assign sum=a^b^cin; 
 assign carry=(a & b) | (b & cin) | (cin & a); 
 endmodule

full subtracter:
module fullsubtracter(a, b, cin, diff, borrow); 
    input a; 
    input b; 
    input cin; 
    output diff; 
    output borrow; 
  wire abar; 
  assign abar= ~ a; 
  assign diff=a^b^cin; 
  assign borrow=(abar & b) | (b & cin) |(cin & abar); 
 
endmodule
```

Developed by : sharan I 
RegisterNumber:24010956
*/

**RTL Schematic**
full adder:
![exp-4-d](https://github.com/user-attachments/assets/59352b54-d0d4-46c9-8b6f-e1cad2e8b2f9)

full subtracter:
![exp-4 2-d](https://github.com/user-attachments/assets/4974d185-82cc-4446-8f11-e0bcf7e26382)

**Output Timing Waveform**
full adder:
![exp-4-w](https://github.com/user-attachments/assets/f3fdba19-b0cb-4dc9-84b4-a200ef0c43f4)

full subtracter:
![exp-4 2-w](https://github.com/user-attachments/assets/121ab902-cb67-4aae-8441-27feb522d748)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



