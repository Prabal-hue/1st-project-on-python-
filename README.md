# 🐍 My First Python Project

A clean, beginner-friendly Python application hosted on GitHub to demonstrate foundational programming logic, console I/O handling, and conditional statements.

## 🚀 Project Overview
This repository serves as a practical milestone for learning the core fundamentals of Python. It demonstrates:
* Direct user input handling via the console.
* Implementation of conditional flow control (`if/elif/else`).
* Clean, readable code structure following basic Python paradigms.

## 🛠️ Built With
* **Language:** Python 3.x
* **Version Control:** Git & GitHub

## 🏃 How to Run the Project Locally

If you want to test this code on your machine, follow these simple steps:

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/Prabal-hue/1st-project-on-python-.git](https://github.com/Prabal-hue/1st-project-on-python-.git)

    choice = input("Enter your choice (1-4): ")

    if choice == '1':
        # Add Expense
        date = input("Enter date (DD-MM-YYYY): ")
        category = input("Enter category (Food, Travel, Shopping, etc): ")
        description = input("Enter short description: ")
        try:
            amount = float(input("Enter amount (₹): "))
            if amount <= 0:
                print(" Amount must be a positive number.")
                continue
            expense = {
                "date": date,
                "category": category,
                "description": description,
                "amount": amount
            }
            expenses.append(expense)
            print(" Expense added successfully!")
        except ValueError:
            print(" Invalid amount. Please enter a number.")

    elif choice == '2':
        # View All Expenses
        if not expenses:
            print(" No expenses recorded yet.")
        else:
            print("\n--- All Recorded Expenses ---")
            for i, expense in enumerate(expenses):
                print(f"{i+1}. Date: {expense['date']}, Category: {expense['category']}, "
                      f"Description: {expense['description']}, Amount: ₹{expense['amount']:.2f}")
            print("-----------------------------\n")

    elif choice == '3':
        # View Total Spending
        if not expenses:
            print(" No expenses recorded yet to calculate total spending.")
        else:
            total_spending = 0
            for expense in expenses:
                total_spending += expense['amount']
            print(f"💰 Total Spending = ₹{total_spending:.2f}")

    elif choice == '4':
        # Exit
        print(" Exiting Expense Tracker. Goodbye!")
        break

    else:
        print(" Invalid choice. Please enter a number between 1 and 4.")






