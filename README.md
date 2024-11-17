# NAME: JAYAGAR.T
# REG.NO: 24901219
# EXPERIMENT-4: FULL ADDER AND SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

# AIM:

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

# EQUIPMENTS REQUIRED:

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

# FULL ADDER AND FULL SUBTRACTOR

# FULL ADDER

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

### Figure -1 FULL ADDER

# FULL SUBTRACTOR

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin



# PROCEDURE:
Full Adder
Inputs: Three inputs: A, B (the two bits to be added), and Cin (the carry-in bit from a previous addition). Outputs: Two outputs: Sum (the resulting sum) and Cout (the carry-out bit). Logic: Sum = A ^ B ^ Cin (XOR operation). Cout = (A & B) | (A & Cin) | (B & Cin) (carry occurs if at least two inputs are 1).

Full Subtractor
Inputs: Three inputs: A, B (the two bits, where A - B is calculated), and Bin (the borrow-in from a previous subtraction). Outputs: Two outputs: Diff (the resulting difference) and Bout (the borrow-out bit). Logic: Diff = A ^ B ^ Bin (XOR operation). Bout = (~A & B) | ((~A | B) & Bin) (borrow occurs if A is less than B or needs a borrow). Both circuits follow simple XOR logic for the primary result and AND-OR logic to determine carry or borrow conditions.

# Program:

#### module fulladdsub(a,b,cin,bin,sum,carry,difference,borrow);
#### input a,b,cin,bin;
#### output sum,carry,difference,borrow;
#### assign sum=a^b^cin;
#### assign carry=(a^b)&cin|a&b;
#### assign difference=a^b^bin;
#### assign borrow=~(a^b)&bin|(~a)&b;
#### endmodule
# TRUTH TABLE:
![WhatsApp Image 2024-11-16 at 20 10 16_814a4975](https://github.com/user-attachments/assets/77825725-3da0-40a7-a1df-bfdac9d46d14)

![WhatsApp Image 2024-11-16 at 20 10 28_1b5f180f](https://github.com/user-attachments/assets/6bf9f439-8a43-4d6e-ad35-38c4d34f1c7f)


# RTL OUTPUT:
![WhatsApp Image 2024-11-16 at 20 09 45_da6240e8](https://github.com/user-attachments/assets/21674ae2-d8ae-4636-8c8c-a78b16881d27)


 # OUTPUT WAVEFORM:
 ![WhatsApp Image 2024-11-16 at 20 10 02_85ac57ee](https://github.com/user-attachments/assets/39b85cf4-dcc0-4737-acb3-849ad5ed06ed)

# RESULT:

 The Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



