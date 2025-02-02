# AI-Fraud-Detection-Revenue-Assurance


Key Columns for Fraud Detection & Revenue Assurance Analysis:
`Customer & Account Information:`

- customerId / CustomerID: Unique identifier for customers.
- accountNumber: Account identifier.
- creditLimit: Credit limit for the account.
- availableMoney: Available money in the account, useful for fraud detection.
- currentBalance: Current balance in the account.
- accountOpenDate: Date the account was opened.
- dateOfLastAddressChange: Helps identify anomalies in account activity.

`Transaction Information:`

- transactionAmount: The amount for each transaction, critical for spotting unusual or fraudulent amounts.
- transactionDateTime: Timestamp of each transaction, which can be useful for time-based fraud detection.
- transactionType: Indicates whether a transaction is a purchase, refund, or any other type, useful for identifying suspicious activity.
- OrderID: Unique order identifier, which is useful for tracking specific transactions.
- ProductInformation: Describes the product being purchased, valuable for identifying anomalies or fraudulent product-related transactions.
- PurchaseDate: The date of the purchase, useful for detecting patterns or unusual activity.
- Location: Can help identify if the transaction is occurring from a suspicious or unexpected location.

`Fraud Detection Specific Columns:`

isFraud: Target column for fraud detection model, indicating whether the transaction is fraudulent or not.
cardCVV / enteredCVV: CVV details for verifying credit card authenticity.
cardLast4Digits: Last four digits of the card number, useful for tracing transactions.
merchantName: Name of the merchant where the transaction took place.
merchantCountryCode: Useful for identifying geographical anomalies in fraud.
merchantCategoryCode: Merchant category could be used for identifying unusual transaction types.
posEntryMode: Identifies the mode of entry (e.g., swipe, chip, etc.), which could indicate potential fraudulent behavior.
Telecom Usage Information (Relevant for Churn Prediction and Risk):

state: Customer's location, which can help in location-based fraud detection.
area code: Useful for telecom-related fraud.
account length: Indicates how long the customer has been with the company, which could influence churn and fraud risk.
number vmail messages: Can be used to assess customer engagement and behavior.
total day minutes, total day calls, total day charge: Data usage patterns that may indicate fraudulent activity or changes in behavior.
total eve minutes, total eve calls, total eve charge: Evening usage patterns.
total night minutes, total night calls, total night charge: Night usage patterns.
total intl minutes, total intl calls, total intl charge: International usage, which may flag fraudulent or out-of-pattern transactions.
customer service calls: The number of times the customer has contacted customer service, useful for detecting potentially fraudulent behavior.
Churn Prediction:

churn: Indicates whether the customer has churned, which can be used for predictive analysis.
Columns to Potentially Drop or Ignore:
Unnamed: 0: This is typically an index column or irrelevant column created during data import. You can drop it.
common_id: Depending on the context, it might not provide relevant information.
transactionType, posConditionCode, expirationDateKeyInMatch, cardPresent: These could be more relevant for specific fraud models, but may not be necessary for all types of fraud detection
