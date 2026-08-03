# Half-Adder
first verylog
# Half Adder Program

# Take two binary inputs
A = int(input("enter first bit (0 or 1): "))
B = int(input("enter second bit (0 or 1): "))
# Calculate Sum and curry
Sum = A ^ B 
Carry = A & B
print("Sum =",Sum)
print("Carry =",Carry)
