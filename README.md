# Credit Card Company Spending Alert System

## Problem Statement

- Develop a system for a credit card company to provide alerts to users when their spending in any particular category is significantly higher than usual.
- Compare the total amount paid for the current month, grouped by category, with the previous month.
- Filter down to the categories for which the user spent at least 50% more this month than last month.
- Compose an email message to the user that lists the categories for which spending was unusually high.

## Classes and Variables

### CreditCardUser:
- Variables:
  - `name`: Name of the credit card user.
  - `email`: Email address of the credit card user.
- Methods:
  - `get_name()`: Retrieve the name of the credit card user.
  - `get_email()`: Retrieve the email address of the credit card user.

### Transaction:
- Variables:
  - `category`: Category of the transaction (e.g., groceries, travel).
  - `amount`: Amount spent in the transaction.
  - `date`: Date of the transaction.
- Methods:
  - `get_category()`: Retrieve the category of the transaction.
  - `get_amount()`: Retrieve the amount spent in the transaction.
  - `get_date()`: Retrieve the date of the transaction.

### TransactionHistory:
- Variables:
  - `transactions`: List of transactions made by the user.
- Methods:
  - `add_transaction(transaction)`: Add a new transaction to the transaction history.
  - `get_transactions()`: Retrieve the list of transactions.
  - `filter_by_month(month, year)`: Filter transactions by a specific month and year.
  - `group_by_category()`: Group transactions by category.
  - `calculate_total_spending_per_category()`: Calculate total spending per category.
  - `compare_previous_month()`: Compare total spending of the current month with the previous month.

### SpendingAlertSystem:
- Variables:
  - `threshold_percentage`: Percentage increase threshold for unusual spending.
- Methods:
  - `set_threshold_percentage(threshold)`: Set the threshold percentage for unusual spending.
  - `detect_unusual_spending(transaction_history)`: Detect unusually high spending based on the provided transaction history.
  - `compose_alert_email(user, unusual_spending_categories)`: Compose an email alert for the user listing the unusually high spending categories.

## Note:
- Ensure proper error handling for invalid inputs and edge cases.
- Implement necessary validation for transactions and user data.
- Utilize appropriate data structures for efficient data handling.
- Test the system thoroughly to ensure its correctness and reliability.
