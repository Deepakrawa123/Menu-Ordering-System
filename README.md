# Menu-Ordering-System
 🏨 Deepak Hotel Menu Ordering System

Welcome to the **Deepak Hotel Menu Ordering System** – a basic Python-based console application that simulates a customer placing food orders from a menu.

## 📋 Description

This project allows users to:

- View a menu with items and prices.
- Place an order for one or two items.
- Get feedback on whether the item is available.
- View the total bill at the end.

It demonstrates basic Python concepts such as:

- Dictionaries
- Conditional statements
- User input handling
- String formatting

## 🚀 Getting Started

### Prerequisites

- Python 3.x installed on your machine

### Running the Program

1. Clone the repository or download the `.py` file.
2. Open your terminal or command prompt.
3. Navigate to the project directory.
4. Run the script:

```bash
python hotel_menu.py

# Define the menu as a dictionary
menu = {
    'Pizza': 100,
    'Burger': 50,
    'Pasta': 70,
    'Salad': 30,
    'Sandwich': 40,
    'Cold Drinks': 30
}

# Greeting
print("Welcome to Deepak Hotel")
print("Here is our menu:")
for item, price in menu.items():
    print(f"{item}: ₹{price}")

# Taking order
order_total = 0

item_1 = input("Enter the item you want to order: ").title()
if item_1 in menu:
    order_total += menu[item_1]
    print(f"Your item '{item_1}' is added to your order.")
else:
    print(f"Sorry, '{item_1}' is not available in the menu.")

another_order = input("Do you want to order another item? (yes/no): ").lower()
if another_order == "yes":
    item_2 = input("Enter the second item: ").title()
    if item_2 in menu:
        order_total += menu[item_2]
        print(f"Your item '{item_2}' is added to your order.")
    else:
        print(f"Sorry, '{item_2}' is not available in the menu.")

print(f"Your total bill is: ₹{order_total}")
