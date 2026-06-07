## Conversion from One Base to Another
1. **Convert the decimal number 156 to:**
   - Binary
   - Octal
   - Hexadecimal

2. **Convert the binary number 101101 to:**
   - Decimal
   - Octal
   - Hexadecimal

3. **Convert the octal number 745 to:**
   - Decimal
   - Binary
   - Hexadecimal

4. **Convert the hexadecimal number 3F9 to:**
   - Decimal
   - Binary
   - Octal

 oct1 = oct(dec1)[2:]
... hex1 = hex(dec1)[2:].upper()
...
... print(f"1. Decimal 156:")
... print(f"   - Binary: {bin1}")
... print(f"   - Octal: {oct1}")
... print(f"   - Hexadecimal: {hex1}")
...
... # Question 2: Binary 101101
... bin2 = "101101"
... dec2 = int(bin2, 2)
... oct2 = oct(dec2)[2:]
... hex2 = hex(dec2)[2:].upper()
...
... print(f"2. Binary 101101:")
... print(f"   - Decimal: {dec2}")
... print(f"   - Octal: {oct2}")
... print(f"   - Hexadecimal: {hex2}")
...
... # Question 3: Octal 745
... oct3 = "745"
... dec3 = int(oct3, 8)
... bin3 = bin(dec3)[2:]
... hex3 = hex(dec3)[2:].upper()
...
... print(f"3. Octal 745:")
... print(f"   - Decimal: {dec3}")
... print(f"   - Binary: {bin3}")
... print(f"   - Hexadecimal: {hex3}")
...
... # Question 4: Hexadecimal 3F9
... hex4 = "3F9"
... dec4 = int(hex4, 16)
... bin4 = bin(dec4)[2:]
... oct4 = oct(dec4)[2:]
...
... print(f"4. Hexadecimal 3F9:")
... print(f"   - Decimal: {dec4}")
... print(f"   - Binary: {bin4}")
... print(f"   - Octal: {oct4}")
