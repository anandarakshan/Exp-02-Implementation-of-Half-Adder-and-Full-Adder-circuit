## Name : Ananda Rakshan K V

## Roll.No : 212223230014

# Exp-03-Implementation of Half Adder and Full Adder circuit

  Implementation-of-Half-Adder-and-Full-Adder-circuit
  
## AIM:

To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

## Theory:

Adders are digital circuits that carry out addition of numbers.

## Half Adder:

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

## Full Adder:

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER :


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER :

## Procedure:

•Connect the supply (+5V) to the circuit

•Switch ON the main switch

•If the output is 1, then the led glows.

## Program:

#### Half-adder:

module halfadder(a,b,sum,carry);

input a,b;

output sum,carry;

xor (sum,a,b);

and (carry,a,b);

endmodule

#### Full-adder:

module fulladder(a,b,c,sum,carry);

input a,b,c;

output sum,carry;

xor (sum,a,b,c);

assign carry=a&b | b&c | a&c;

endmodule

## Truthtable:

#### Half-adder:

![Truth table-halfadder](https://github.com/anandarakshan/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/139217934/3b915795-1807-47ef-aefb-c6baedc0fa98)

#### Full-adder:

![Truth table-fulladder](https://github.com/anandarakshan/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/139217934/d1fe435a-cf38-441c-b8d2-0421ee914b38)

## RTL realization:

#### Half-adder:

![RTL-halfadder](https://github.com/anandarakshan/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/139217934/ef77bab0-c8aa-42e2-8be0-b0c359fbc987)

#### Full-adder:

![RTL-fulladder](https://github.com/anandarakshan/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/139217934/0bc8d450-9831-49c1-a185-960faa6ee5a5)

## TIMING DIAGRAM:

#### Half-adder:

![halfadder-waveform](https://github.com/anandarakshan/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/139217934/d14a0c56-9ab5-46ff-8253-ccfdc7d309fd)

#### Full-adder:

![fulladder-waveform](https://github.com/anandarakshan/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/139217934/db72b1d0-10da-448e-85f0-a771ee227e5c)

## Result:

To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.
