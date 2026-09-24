# ExpenseMate MongoDB Schema

## Collections

### users
Stores registered user information.

### categories
Stores income and expense categories for each user.

### transactions
Stores all income and expense transactions.

### budgets
Stores spending limits created by users.

### savingsGoals
Stores user savings targets and progress.

### recurringTransactions
Stores recurring income and expense transactions.

### notifications
Stores reminders and financial notifications.

## Relationships

users
  ├── transactions
  ├── categories
  ├── budgets
  ├── savingsGoals
  ├── recurringTransactions
  └── notifications

categories
  ├── transactions
  └── budgets
