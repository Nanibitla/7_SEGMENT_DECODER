# 4-Bit BCD to 7-Segment Display Decoder

## 📌 Project Overview

This project implements a **4-bit BCD (Binary-Coded Decimal) to 7-segment display decoder** using **Logisim Evolution**.

The circuit accepts a 4-bit BCD input and displays the corresponding decimal digit from **0 to 9** on a 7-segment display.

The project was designed using basic digital logic gates and Boolean expressions for each of the seven segments.

## 🎯 Objective

- Convert a 4-bit BCD input into a 7-segment display output.
- Understand how Boolean expressions can control individual display segments.
- Implement and verify a combinational digital logic circuit.
- Gain practical experience with Logisim Evolution.

## 🔢 Input and Output

### Input

The circuit uses four input bits:

- `A` – Most Significant Bit (MSB)
- `B`
- `C`
- `D` – Least Significant Bit (LSB)

### Output

The output controls seven segments:

`a, b, c, d, e, f, g`

The display represents decimal digits **0–9**.

Inputs from `1010` to `1111` are invalid BCD combinations.

## 🧮 Boolean Expressions

The seven segment outputs are implemented using the following Boolean expressions:

a = A + C + (B XNOR D)

b = B' + (C XNOR D)

c = C' + D + B

d = (D' + C)B' + A + B'C + BC'D

e = (B' + C)D'

f = A + (B + C')D' + BC'

g = A + (B' + D')C + BC'
