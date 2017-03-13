
# About the data

The original dataset has 38593 records, which is an entire year of expenses.
Expenses are divided in 42 groups. Each group has different categories (1 to n). We are trying to predict categories for a given group according to its expense description. Additional columns like account number, supplier, source, and reference might be considered as parameters.
The first group to analyse is Car Expenses, which has 2899 records and 9 categories.

* GROUP        object  (Car expenses)


* ID_ACC        int64  (Account, it is actually a code so it is going to be handled as string)


* SUB_GROUP     int64  (It is actually a code so it is going to be handled as string)


* ID_SUP       object  (Supplier)


* ID_JOU       object  (Type of Journal)


* MONTH         int64  (Expense Month)


* SOURCE       object  (Source system of the expense: SAP, ORA, etc...)


* REF          object  (Transaction reference, it can be a date, a code, a number,...)


* DESC         object  (Description, it is a free text of 30 characters maximum)


* AUX1         object  (It is a substring of the description. It could be the category, but it is not always correct)


* DB           object  (Source database)


* ID_CC         int64  (Cost Center, it is actually a code so it is going to be handled as string)


* !!! CATEGORY     object  (This is the field to be predicted)


* VALUE         int64  (It is the amount of the expense)


* COUNT         int64  (It has a value of 1 for each row)



In the Car Expenses sample dataset are  2 subgroups, 6 accounts, 85 suppliers, 14 sources, 6 journal types, 555 references, 276 descriptions, 13 aux categories, 2 databases, 62 cost centers, and 9 Categories 

#### Strategy to follow

Bag-of-words

As a first attempt to classify the expenses in categories, a Bag-of-Words strategy is going to be used. A single "sentence" is created using: 
* Account 
* Supplier 
* Journal Type
* Source 
* Aux category 
* Cost Center 
* Description

The "sentence" is going to be used as a parameter to clasify rows into categories using Naïve Bayes Classification


```python

```
