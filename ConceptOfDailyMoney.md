# Introduction #
<p>
This page shows concept of daily-money, since it is android application, I will keep every thing as simple as possible.<br>
</p>
<p>
The basic idea is money was transfered from one account to another, user record the detail for each transfer with his android phone. This application helps user to record detail, shows weekly/monthly/weekly report and mails csv through the android phone.<br>
</p>

# Account Type #
<p>
There are 5 types of account type:<br>
<ul><li>Income<br>
</li><li>Expense<br>
</li><li>Asset<br>
</li><li>Liability<br>
</li><li>Other<br>
</p></li></ul>

# Account #
<p>
User can create multiple account with a name , initial value, account type and initial value(money) for total balance counting.<br>
</p>

# Detail/Transaction #
<p>
For each daily-money detail record, user have to fill following data.<br>
<ul><li>date<br>
</li><li>from account<br>
</li><li>to account<br>
</li><li>value (money)<br>
</li><li>note<br>
</p>
<h1>Rules of single month/year balance counting</h1>
<p>
</li><li>INCOME = ΣFrom Detail.value<br>
</li><li>EXPENSE = ΣTo Detail.value<br>
</li><li>ASSET = ΣTo Detail.value - ΣFrom Detail.value<br>
</li><li>LIABILITY = ΣFrom Detail.value - ΣTo Detail.value<br>
</li><li>OTHER = = ΣTo Detail.value - ΣFrom Detail.value<br>
</p></li></ul>

# Rules of total balance counting #
<p>
<ul><li>INCOME = Σinit + ΣFrom Detail.value<br>
</li><li>EXPENSE = Σinit + ΣTo Detail.value<br>
</li><li>ASSET = Σinit + ΣTo Detail.value - ΣFrom Detail.value<br>
</li><li>LIABILITY = Σinit + ΣFrom Detail.value - ΣTo Detail.value<br>
</li><li>OTHER = = Σinit + ΣTo Detail.value - ΣFrom Detail.value<br>
</p>
<p>
all archived Details are not editable and not included in total balance counting.<br>
</p>
<p>
the initial value of Asset type account will be updated after Details archived.<br>
</p>