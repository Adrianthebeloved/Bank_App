# Skillup Africa Beneficiary Challenge

## Project Brief- Backend Developers 

Write a Python program that allows customers to: 
a. `Create` an account with the account number generated if they do not have an account. All generated account numbers should begin with 0 b. Log in to the program if they have an account 
c. `Deposit` money 
d. `Withdraw` money from the account if they have a sufficient amount. e. Users should be able to `transfer` money to other users in the account 
f. Users should be able to `check` their account balances.

The program should keep running until the user decides to make it log out and/or quit. 
The account data should be stored in a dictionary that looks like this:

```json
data = { 
- "0123445677" : { 
- "first_name":"John", 
- "last_name" : "Doe ", 
- "login_pin" : "8424",
- "transaction_pin" : "0934", 
- "balance" : 0 }
}
```
### Install Dependencies

1. **Python 3.7** - Follow instructions to install the latest version of python for your platform in the [python docs](https://docs.python.org/3/using/unix.html#getting-and-installing-the-latest-version-of-python)

2. **Virtual Environment** - We recommend working within a virtual environment whenever using Python for projects. This keeps your dependencies for each project separate and organized. Instructions for setting up a virual environment for your platform can be found in the [python docs](https://packaging.python.org/guides/installing-using-pip-and-virtual-environments/)

### Set up Storage for Persistence

The dictionary which contains users details is stored in a .txt file. So navigate to your project folder and create a .txt file containing an empty dictionary.
```json
with open('bank_app_db.txt', 'r') as file:
    data = eval(file.read())
```
and
```json
with open('bank_app_db.txt', 'w') as file:
    file.write(str(data))
```
for persistence

### Documentation

The project makes use of the following functions:

`def deposit()`

- To deposit money.

`def withdraw()`

- To withdraw money if user balance is sufficient.

`def account_num()`

- To generate a random account number starting with '0' 