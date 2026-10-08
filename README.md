# interncircle
def arithmetic():
    print("\n--- Arithmetic Calculator ---")

    while True:
        try:
            a = float(input("Enter first number: "))
            b = float(input("Enter second number: "))
            break
        except ValueError:
            print("Invalid input! Please enter numbers.")

    print("1. Addition")
    print("2. Subtraction")
    print("3. Multiplication")
    print("4. Division")

    while True:
        choice = input("Choose operation (1-4): ")

        if choice == "1":
            print("Result:", a + b)
            break
        elif choice == "2":
            print("Result:", a - b)
            break
        elif choice == "3":
            print("Result:", a * b)
            break
        elif choice == "4":
            if b == 0:
                print("Cannot divide by zero!")
            else:
                print("Result:", a / b)
                break
        else:
            print("Invalid choice!")


def unit_conversion():
    print("\n--- Unit Converter ---")
    print("1. Kilometres to Miles")
    print("2. Celsius to Fahrenheit")

    while True:
        choice = input("Choose conversion (1-2): ")

        if choice == "1":
            while True:
                try:
                    km = float(input("Enter kilometres: "))
                    break
                except ValueError:
                    print("Please enter a valid number.")

            miles = km * 0.621371
            print("Miles:", miles)
            break

        elif choice == "2":
            while True:
                try:
                    c = float(input("Enter Celsius: "))
                    break
                except ValueError:
                    print("Please enter a valid number.")

            f = (c * 9 / 5) + 32
            print("Fahrenheit:", f)
            break

        else:
            print("Invalid choice!")


def currency_conversion():
    print("\n--- Currency Converter ---")
    print("1. USD to INR")
    print("2. INR to USD")

    # Sample fixed rates
    usd_to_inr = 90
    inr_to_usd = 1 / usd_to_inr

    while True:
        choice = input("Choose conversion (1-2): ")

        if choice == "1":
            try:
                usd = float(input("Enter USD: "))
                print("INR:", usd * usd_to_inr)
                break
            except ValueError:
                print("Please enter a valid number.")

        elif choice == "2":
            try:
                inr = float(input("Enter INR: "))
                print("USD:", inr * inr_to_usd)
                break
            except ValueError:
                print("Please enter a valid number.")

        else:
            print("Invalid choice!")


# Main program
while True:
    print("\n==============================")
    print(" INTERACTIVE CALCULATOR")
    print("==============================")
    print("1. Arithmetic Calculator")
    print("2. Unit Converter")
    print("3. Currency Converter")
    print("4. Exit")

    choice = input("Enter your choice (1-4): ")

    if choice == "1":
        arithmetic()

    elif choice == "2":
        unit_conversion()

    elif choice == "3":
        currency_conversion()

    elif choice == "4":
        print("Thank you for using the calculator!")
        break

    else:
        print("Invalid choice! Please try again.")
