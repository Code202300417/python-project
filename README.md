# python-project

class BankAccount:
    def __init__(self, owner, balance):
        self.owner = owner  # Corrected attribute name
        self.balance = balance  # Corrected attribute name

    def deposit(self, amount):
        self.balance += amount  # Updated balance logic
        print(f"Vista Bank has deposited {amount} in your account.")

    def get_balance(self):
        return self.balance  # Added method to return balance


# Main program
account = BankAccount("Samuel Sillah", 0)
account.deposit(1000)
print(f"Current balance: {account.get_balance()}")

while True:
    print("\nMenu:")
    print("1. Deposit")
    print("2. Check Balance")
    print("3. Exit")

    choice = input("Please select your choice: ")

    if choice == "1":
        amount = float(input("Enter the amount to deposit: "))
        account.deposit(amount)
    elif choice == "2":
        print(f"Your current balance is: {account.get_balance()}")
    elif choice == "3":
        print("Thank you for using Vista Bank. Goodbye!")
        break
    else:
        print("Invalid choice. Please try again.")

