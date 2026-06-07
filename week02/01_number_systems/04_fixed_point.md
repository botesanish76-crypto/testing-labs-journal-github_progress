
## Fixed Point Representation
**Represent the decimal number in fixed-point binary:**
   - 12.75 with 4 bits for the integer part and 4 bits for the fractional part
   - 5.125 with 3 bits for the integer part and 5 bits for the fractional part
   - 7.5 with 4 bits for the integer part and 4 bits for the fractional part
   - 
 def to_fixed_point(decimal_num, int_bits, frac_bits):
    integer_part = int(decimal_num)
    fractional_part = decimal_num - integer_part
    
    integer_bin = bin(integer_part)[2:].zfill(int_bits)
    
    fractional_bin = ""
    while len(fractional_bin) < frac_bits:
        fractional_part *= 2
        bit = int(fractional_part)
        fractional_bin += str(bit)
        fractional_part -= bit
        
    return f"{integer_bin}.{fractional_bin}"

print(to_fixed_point(12.75, 4, 4))
print(to_fixed_point(5.125, 3, 5))
print(to_fixed_point(7.5, 4, 4))
