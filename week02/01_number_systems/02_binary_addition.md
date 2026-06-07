## Adding Binary Numbers
   - 1011 + 1101
   - 100110 + 101011
   - 11101 + 10111

## Subtracting Binary Numbers
   - 1101 - 1010
   - 10110 - 1001
   - 10001 - 1110
   - additions = [
    ("1011", "1101"),
    ("100110", "101011"),
    ("11101", "10111")
]

subtractions = [
    ("1101", "1010"),
    ("10110", "1001"),
    ("10001", "1110")
]

print("Additions:")
for a, b in additions:
    res = bin(int(a, 2) + int(b, 2))[2:]
    print(f"{a} + {b} = {res}")

print("\nSubtractions:")
for a, b in subtractions:
    res = bin(int(a, 2) - int(b, 2))[2:]
    print(f"{a} - {b} = {res}")
