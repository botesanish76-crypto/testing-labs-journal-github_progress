
## Limits of Binary Representation
**Determine the limits of binary representation:**
   - Largest positive number with 8 bits in unsigned binary
   - Largest positive number with 8 bits in signed binary (two's complement)
   - Smallest negative number with 8 bits in signed binary (two's complement)
unsigned_max = (1 << 8) - 1
signed_max = (1 << 7) - 1
signed_min = -(1 << 7)

print(f"Unsigned Max: {unsigned_max} ({bin(unsigned_max)[2:]})")
print(f"Signed Max: {signed_max} (0{bin(signed_max)[2:]})")
print(f"Signed Min: {signed_min} ({bin(256 + signed_min)[2:] if signed_min < 0 else bin(signed_min)[2:]})")
