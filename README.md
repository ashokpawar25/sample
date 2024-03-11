# Unusual Spends Alert System

## Problem Statement

 -You work at a credit card company and as a value-add they want to start providing alerts to users when their spending in any particular category is higher than usual.
 - Compare the total amount paid for the current month, grouped by category with the previous month 
 - Filter down to the categories for which the user spent at least 50% more this month than last month
 - Compose an e-mail message to the user that lists the categories for which spending was    unusually high

## Classes and Variables

### User:
- States:
  - `userId`:Unique id of user.
  - `name`:Name of the credit card user.
  - `email`:Email address of the credit card user.
- Constructor:
  -`User(int userId, String name, String email)`

- Behaviour:
  - `getUserId`: Retrieve the user id of user.
  - `getName()`: Retrieve the name of user.
  - `getEmail()`: Retrieve the email address of user.

### Transaction:
- States:
  - `transactionId`: Unique Id of Transaction.
  - `category`: Category of the transaction (e.g., groceries, travel).
  - `amount`: Amount of transaction.
  - `date`: Date of the transaction.
  - `userId`: User who did transaction.
- Constructor:
  -`Transaction(int transactionID, String category, int amount, LocalDate transactionDate, int userId)`
- Behaviour:
  - `getTransactionId`: Retrive transaction id.
  - `getCategory()`: Retrieve the category of the transaction.
  - `getAmount()`: Retrieve the amount spent in the transaction.
  - `getDate()`: Retrieve the date of the transaction.
  - `getUserId`: Get the User who did transaction.

### TransactionHistory:
- States:
  - `transactions`: List of transactions made by the user.
- Behaviour:
  - `addTransaction(Transaction transaction)`: Add a new transaction to the transaction history.
  - `getAllTransactions()`: Retrieve the list of transactions.
  - `filterTransactionByCurrentMonth()`: Filter transactions for current month.
  - `filterTransactionByPreviousMonth()`:Filter transactions for previous month.
  - `filterTransactionByCatgory(String catogory)`: Filter transactions by category.
  - `ComparePreviouMonthSpending()`: Compare total spending of the current month with the previous month.

### ExtraPayUsers:
-States:
 -`userId`: Id of user who is doing extra spent.
 -`category`: On which category they spent.
 -`moreSpentAmount`: How much extra they are paying.

-Behaviour:
  -`getUserId()`: Retrieve Id Of user.
  -`getCategory()`: Retrieve category.
  -`getMoreSpentAmount()`: get Amount Of extra spent.


### UserHandler:
-States:
  -`List<User>`: To sotre the information of user.

-Behaviour:
 -`addUser(User user)`: Add new user.
 -`getUserByUserId(int userId1)`: Retrieve data of specific user
  

### SendEmail:
- Behaviour:
  - `sendEmail(String subject, String body, String bEmail)`: Send mail to user.
