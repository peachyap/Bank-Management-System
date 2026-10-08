# Bank Management System

A console banking program written in C++ for my first-year programming course. It creates accounts, lists and searches them, and handles deposits and withdrawals.

**Live demo:** [Interactive dashboard](PASTE-YOUR-LINK-HERE)

## Features

1. Create a new account (name, account number, opening balance)
2. Show all accounts
3. Search for an account by number
4. Deposit money
5. Withdraw money (refused if the balance is too low)
6. Exit

## How it works

- `BankAccount` stores one customer's name, account number and balance. The fields are private and accessed through getters.
- `BankManagement` keeps all accounts in a `vector<BankAccount>` and provides adding, listing, searching and lookup.
- `findAccount()` returns a pointer to the stored account, so deposits and withdrawals change the real balance.
- `main()` runs a menu loop with `do-while` and `switch`.

## Build and run

```bash
g++ bank_management_system.cpp -o bank
./bank
```

On Windows, run `bank.exe` instead. The program uses `system("cls")` to clear the screen, so on Mac or Linux you will see a harmless "cls" error line each time the menu redraws.

## Known limitations

- `findAccount()` has no return value when no account matches.
- Negative amounts and duplicate account numbers are accepted.
- Names are read with `cin >>`, so they stop at the first space.
- Accounts are held in memory only and are lost when the program exits.
- Searching for a missing account prints nothing.

## Concepts practised

Classes and objects, encapsulation, composition, `std::vector`, pointers, control flow, and basic input checking.
