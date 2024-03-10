# Unusual Spends Alert System

## Problem Statement

 -You work at a credit card company and as a value-add they want to start providing alerts to users when their spending in any particular category is higher than usual.
 - Compare the total amount paid for the current month, grouped by category with the previous month 
 - Filter down to the categories for which the user spent at least 50% more this month than last month
 - Compose an e-mail message to the user that lists the categories for which spending was    unusually high

## Classes and Variables

### CardUser:
- Variables:
  - `userId`: Unique id of user.
  - `name`: Name of the credit card user.
  - `email`: Email address of the credit card user.
- Methods:
  - `get_name()`: Retrieve the name of the credit card user.
  - `get_email()`: Retrieve the email address of the credit card user.

### Transaction:
- Variables:
  - `transactionId`: Unique Id of Transaction.
  - `category`: Category of the transaction (e.g., groceries, travel).
  - `amount`: Amount of transaction.
  - `date`: Date of the transaction.
  - `userId`: User who did transaction.
- Methods:
  - `getTransactionId`: Retrive transaction id.
  - `getCategory()`: Retrieve the category of the transaction.
  - `getAmount()`: Retrieve the amount spent in the transaction.
  - `getDate()`: Retrieve the date of the transaction.
  - `getUserId`: Get the User who did transaction.

### TransactionHistory:
- Variables:
  - `transactions`: List of transactions made by the user.
- Methods:
  - `addTransaction(transaction)`: Add a new transaction to the transaction history.
  - `getTransactions(transactionId)`: Retrieve the list of transactions.
  - `filteBbyMonth(month, year)`: Filter transactions by a specific month and year.
  - `filterByCategory()`: Filter transactions by category.
  - `calculateSpendingPerCategory()`: Calculate total spending per category.
  - `comparePreviousMonth()`: Compare total spending of the current month with the previous month.

### SendEmail:
- Variables:
  - `email`: email address to send mail.
  - `extraSpent`: catrgory wise list of extra spent.
- Methods:
  - `sendMail(email,List<extraSpent)`: Send mail to user.
