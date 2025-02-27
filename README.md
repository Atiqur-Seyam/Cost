# Costimport time

def simple_calculator():
    # Ask for user input
    operation = input("Enter operation (+, -, *, /): ")
    num1 = float(input("Enter first number: "))
    num2 = float(input("Enter second number: "))
    
    start_time = time.time()  # Start time

    if operation == "+":
        result = num1 + num2
    elif operation == "-":
        result = num1 - num2
    elif operation == "*":
        result = num1 * num2
    elif operation == "/":
        if num2 != 0:
            result = num1 / num2
        else:
            result = "Error: Division by zero"
    else:
        result = "Invalid operation"

    end_time = time.time()  # End time
    
    elapsed_time = (end_time - start_time) * 1000  # Convert to milliseconds

    # Print result
    print(f"Result: {result}")
    print(f"Time taken: {elapsed_time:.4f} ms")
    
    # Ensure that time is under 100ms
    if elapsed_time > 100:
        print("Warning: Calculation took longer than 100ms!")
    else:
        print("Calculation completed within 100ms.")

# Run the calculator
simple_calculator()
