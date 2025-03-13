# PLP-Introduction-to-Python-


# Function to perform the mathematical operation

def calculate(num1, num2, operation):
    if operation == '+':
        return num1 + num2
    elif operation == '-':
        return num1 - num2
    elif operation == '*':
        return num1 * num2
    elif operation == '/':
        if num2 != 0:  # Check for division by zero
            return num1 / num2
        else:
            return "Error: Division by zero is not allowed."
    else:
        return "Error: Invalid operation."

# Main program
def main():
    print("Welcome to the Simple Calculator!")
    print("This program asks for two numbers and a mathematical operation (+, -, *, /).")

    try:
        # Ask the user for input
        num1 = float(input("Enter the first number: "))
        num2 = float(input("Enter the second number: "))
        operation = input("Enter the operation (+, -, *, /): ").strip()  # Remove extra spaces

        # Validate the operation input
        if operation not in ['+', '-', '*', '/']:
            print("Error: Invalid operation. Please use one of the following: +, -, *, /")
            return

        # Perform the calculation
        result = calculate(num1, num2, operation)

        # Display the result
        print(f"\nResult: {num1} {operation} {num2} = {result}")

    except ValueError:
        print("Error: Invalid input. Please enter numeric values for the numbers.")

# Run the program
if __name__ == "__main__":
    main()
    
