
## Fixed Point Representation
**Represent the decimal number in fixed-point binary:**
   - 12.75 with 4 bits for the integer part and 4 bits for the fractional part
   - 5.125 with 3 bits for the integer part and 5 bits for the fractional part
   - 7.5 with 4 bits for the integer part and 4 bits for the fractional part

def to_fixed_point(decimal_num, int_bits, frac_bits):
    integer_part = int(decimal_num)
    fractional_part = decimal_num - integer_part

    integer_bin = bin(integer_part)[2:]
    if len(integer_bin) > int_bits:
        raise ValueError(f"Integer part {integer_part} exceeds allocated {int_bits} bits.")
    integer_bin = integer_bin.zfill(int_bits)
    
    fractional_bin = ""
    while len(fractional_bin) < frac_bits:
        fractional_part *= 2
        bit = int(fractional_part)
        fractional_bin += str(bit)
        fractional_part -= bit
        
    return f"{integer_bin}.{fractional_bin}"

cases = [
    {"num": 12.75, "int": 4, "frac": 4},
    {"num": 5.125, "int": 3, "frac": 5},
    {"num": 7.5,   "int": 4, "frac": 4}
]

print(f"{'Decimal':<8} -> {'Fixed-Point Binary (Int.Frac)':<30}")
print("-" * 45)
for case in cases:
    result = to_fixed_point(case["num"], case["int"], case["frac"])
    print(f"{case['num']:<8} -> {result} ({case['int']} bits . {case['frac']} bits)")
