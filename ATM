 Use classes (OOP) ✔ Use encapsulation (private data members) ✔ Implement:
1.Deposit
2.Withdraw
3.Check Balance
4.Save transaction history to a file

C++ Program
C++
#include <iostream>
#include <fstream>
using namespace std;

class ATM {
private:
    int accountNumber;
    string name;
    double balance;

public:
    ATM(int accNo, string userName, double initialBalance) {
        accountNumber = accNo;
        name = userName;
        balance = initialBalance;
    }

    void deposit(double amount) {
        balance += amount;
        saveTransaction("Deposited: " + to_string(amount));
        cout << "Amount deposited successfully.\n";
    }

    void withdraw(double amount) {
        if (amount <= balance) {
            balance -= amount;
            saveTransaction("Withdrawn: " + to_string(amount));
            cout << "Amount withdrawn successfully.\n";
        } else {
            cout << "Insufficient balance!\n";
        }
    }

    void checkBalance() {
        cout << "Current Balance: ₹" << balance << endl;
    }

    void saveTransaction(string transaction) {
        ofstream file("transactions.txt", ios::app);

        if (file.is_open()) {
            file << "Account No: " << accountNumber
                 << " | " << transaction
                 << " | Balance: " << balance << endl;
            file.close();
        }
    }
};

int main() {
    ATM user(1001, "Hasini", 5000);

    int choice;
    double amount;

    do {
        cout << "\n----- ATM MENU -----\n";
        cout << "1. Deposit\n";
        cout << "2. Withdraw\n";
        cout << "3. Check Balance\n";
        cout << "4. Exit\n";
        cout << "Enter choice: ";
        cin >> choice;

        switch (choice) {
        case 1:
            cout << "Enter amount to deposit: ";
            cin >> amount;
            user.deposit(amount);
            break;

        case 2:
            cout << "Enter amount to withdraw: ";
            cin >> amount;
            user.withdraw(amount);
            break;

        case 3:
            user.checkBalance();
            break;

        case 4:
            cout << "Thank you!\n";
            break;

        default:
            cout << "Invalid choice!\n";
        }

    } while (choice != 4);

    return 0;
}
Output Example

----- ATM MENU -----
1. Deposit
2. Withdraw
3. Check Balance
4. Exit

Enter choice: 1
Enter amount to deposit: 1000
Amount deposited successfully.

Current Balance: ₹6000
File Created
A file named transactions.txt will automatically store:

Account No: 1001 | Deposited: 1000 | Balance: 6000
Account No: 1001 | Withdrawn: 500 | Balance: 5500

Concepts Used:
Encapsulation → private variables
Class and Objects
Constructor
File Handling (ofstream)
Conditional statements
Menu-driven program
