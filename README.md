# Tyisha Liggons
# CIS261
# Lab Title: Invoice Line- Item Calculator 

def get_price():
    while True:
        try:
            price = float(input("Enter price: "))
            return price
        except ValueError:
            print("Invalid decimal number. Please try again.")

def get_quantity():
    while True:
        try:
            quantity = int(input("Enter quantity: "))
            return quantity
        except ValueError:
            print("Invalid integer. Please try again.")

def main():
    print("Invoice Line-Item Calculator\n")

    while True:
        price = get_price()
        quantity = get_quantity()
        total = price * quantity

        print(f"PRICE:     {price:.2f}")
        print(f"QUANTITY:  {quantity}")
        print(f"TOTAL:     {total:.2f}\n")

        cont = input("Enter another line item? (y/n): ").lower()
        if cont != 'y':
            print("\nThanks for using the calculator.")
            break

if __name__ == "__main__":
    main()
