## Concept ##
The concept of daily money is very simple
  1. Different accounts (you create accounts depends on your case)
  1. Money transaction between accounts. (you record detail for each transaction)

## Accounts ##
There are 5 types account, you can create/edit/delete it in Account Manager page.
  1. _Income_: salary etc..
  1. _Expense_: food, entertainment etc.
  1. _Asset_: cash, bank
  1. _Liability_: credit card, loan.
  1. _Other_: ...role is like a asset.

  * To sort your account, you just add 1,2,.. or A.B,.. as the prefix of name of account.
  * (Since 0.9.5) Supports hierarchical account name, by .(dot), Ex: Food.lunch, Food.dinner . When editing transaction detail, it provides better selecting of account.

## The transaction detail ##
When you spent some money then you can click the Add Detail on the Main page to create a new record. for example you spent $10 bought a meal, in Detail Editor page, you
  1. select from account :Cash
  1. select to account : Food
  1. select date : today
  1. input money by calculator : 10
  1. input description : hot dog, coke.
  1. click create then click close if no more transaction needs to be created.

above is a very simple use case of daily-money, but, what if your salary is deposit to bank directly, you use credit card buy books on internet? daily-money provide different type of account s, and you could create various accounts against 5 account type.

## Use cases ##
### Salary to Bank ###
**From:** Salary<br />
**To:** Bank
### Bank to Cash ###
**From:** Bank<br />
**To:** Cash
### Buy stuff by credit card ###
**From:** Credit card<br />
**To:** Stuff in expense
### Pay credit card bill by Cash ###
**From:** Cash<br />
**To:** Credit card

## Balance Reports ##
### Ranged Balance ###
In ranged balance reports, I count balance of all the details that you created. The balance is calculated in a time range (current week, current month, current year, or you can change to other range by click the arrow button)

### Cumulated Balance Reports ###
To calculate cumulate balance (ex, how much money I have now, how much cash I have now. not how much I spent this week), you have to set a initial value to a account(normally _Asset_ or _Liability_ type accounts have non-zero initial value. _Income_ and _Expense_ type account should have no initial value). <br />
If you forgot to set initial value of an account, there is a simple way to adjust it. for example ,"I have cash 333, but cumulated balance reports shows I have cash -100)
  1. edit cash account
  1. set initial value of cash to 433 (333 - (-100) )