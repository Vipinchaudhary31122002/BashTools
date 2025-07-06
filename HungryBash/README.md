# 🍽️ Restaurant Order Management Bash Script

This Bash script simulates a simple restaurant order system. It allows customers to view a menu, place orders by selecting item numbers and quantities, and then calculates and displays the total bill along with a personalized message.

## 📄 Features

- Displays a menu read from a `menu.txt` file  
- Allows customers to place an order by entering item numbers and quantities  
- Calculates the total bill based on the selected items  
- Displays a personalized thank-you message with the bill  
- Handles invalid input gracefully  

## 🧰 Requirements

- Linux environment with Bash shell  
- A `menu.txt` file in the same directory as the script, with each menu item in the format:  
```plaintext
ItemName,Price
````
## 📁 Example `menu.txt`
```plaintext
Burger,120
Pizza,250
Pasta,180
Coffee,80
Ice Cream,100
```

## 📦 Usage
```bash
./Restaurant.sh
```

### ✅ How It Works

1. **Menu Display**: The script reads `menu.txt` line-by-line, extracting item names and prices, and displays them with item numbers.
2. **User Input**:
   * Prompts for the customer's name.
   * Asks for item numbers and quantities (e.g., `1 2 3 1` means 2 of item 1 and 1 of item 3).
3. **Order Processing**:
   * Validates input format.
   * Calculates total by matching the selected items with their prices.
4. **Bill Display**:
   * Shows the total bill.
   * Prints a thank-you message using the customer's name.


## 🛑 Input Format
* Enter item numbers and quantities **in pairs**:
```plaintext
1 2 3 1
```
This means:
* 2 × Item 1 (Burger)
* 1 × Item 3 (Pasta)

If the input format is invalid (e.g., text instead of numbers), the script shows an error and exits.

## 🔐 Permissions
To make the script executable:
```bash
chmod +x Restaurant.sh
```

Run the script:
```bash
./Restaurant.sh
```
