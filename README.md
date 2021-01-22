# Detecting-Fraudulent-Transactions

A brief description of data variables is provided in the Variable Description sheet.
Transaction Limit (i.e. maximum amount that could be sent) per transaction is provided for most frequent type of transactions in the last sheet i.e. Transaction Limit sheet.
Transaction data sheet contains transactional data for a period.

- Each Kiosk point is operated by an operator who earns commission for the transactions occurring at its kiosk point. To increase the commission, these operators often do doubtful transactions. Some of these suspicious transactions are:

1. Split transactions (40 Marks) - Transfer of Amount is done by more than one transaction which should have been done by a single transaction.
    Example: An amount of 5,000 could be transferred from account A to account B by a single transaction, but the operator splits it into 3,000 & 2,000 thus increasing the number of transactions at his/her kiosk point.
Note : Each transaction type has a limit per transaction which should be kept in mind while searching for split transactions. For example if the limit is 20,000 for a type of transaction and it is required to transfer 30,000 then splittng the amount in two transactions is necessary and should not be flagged as suspicious transaction

2. Round Trip transactions (60 marks) - Transactions occurring in a circular manner.
    Example: 5,000 is transferred from account A to account B, then the same amount is transferred from account B to account C followed by a transfer of 5,000 from account C to account A thus forming a loop.
The loops can have any number of intermediate accounts.

3. Round + Split transactions (100 marks)
    Example: Account A to Account B ; Rs5,000
             Account B to Account C ; Rs5,000
             Account C to Account A ; Rs2,000
             Account C to Account A ; Rs3,000

The task:
Write a code in R/python to identify above suspicious transactions with minimal usage of loops.
Note: Suspicious transactions to be flagged only if they occur within a day"
