# Database Development

ExpenseMate uses MongoDB to store and manage personal financial data.

## Database Collections

The database will contain the following collections:

### 1. Users
Stores user account and profile information.

Main fields:
- _id
- name
- email
- passwordHash
- createdAt
- updatedAt

### 2. Categories
Stores income and expense categories.

Main fields:
- _id
- userId
- name
- type
- createdAt

### 3. Transactions
Stores all income and expense records.

Main fields:
- _id
- userId
- categoryId
- type
- amount
- description
- transactionDate
- createdAt

### 4. Budgets
Stores user-defined spending budgets.

Main fields:
- _id
- userId
- categoryId
- amount
- startDate
- endDate
- createdAt

### 5. Savings Goals
Stores financial savings goals.

Main fields:
- _id
- userId
- name
- targetAmount
- currentAmount
- targetDate
- createdAt

### 6. Recurring Transactions
Stores recurring income and expense information.

Main fields:
- _id
- userId
- categoryId
- type
- amount
- frequency
- nextDate
- createdAt

### 7. Notifications
Stores financial reminders and system notifications.

Main fields:
- _id
- userId
- title
- message
- type
- isRead
- createdAt

## Database Relationships

- One user can have many transactions.
- One user can have many categories.
- One user can have many budgets.
- One user can have many savings goals.
- One user can have many recurring transactions.
- One user can have many notifications.
- Transactions and budgets can be associated with categories.

## MongoDB Design

MongoDB will use a document-based structure with references between related documents using identifiers such as `userId` and `categoryId`.

Indexes will be added to frequently searched fields such as:

- email
- userId
- transactionDate
- categoryId
