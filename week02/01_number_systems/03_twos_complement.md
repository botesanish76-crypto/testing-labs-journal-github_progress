## Two's Complement
**Find the two's complement of the binary number:**
   - 101010
   - 110011
   - 1001

def twos_complement(binary_str):
    bits = len(binary_str)
    
    ones_complement = "".join('1' if bit == '0' else '0' for bit in binary_str)
    twos_comp_int = int(ones_complement, 2) + 1
    twos_comp_bin = bin(twos_comp_int)[2:].zfill(bits)
    
    if len(twos_comp_bin) > bits:
        twos_comp_bin = twos_comp_bin[-bits:]
        
    return twos_comp_bin

binary_numbers = ["101010", "110011", "1001"]

print("Binary -> Two's Complement")
print("-" * 30)
for num in binary_numbers:
    result = twos_complement(num)
    print(f"{num} -> {result}")
