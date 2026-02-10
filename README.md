#include <iostream>
using namespace std;

int main() {
    int choice;
    double num1, num2;

    cout << "=== Simple Calculator ===\n";

    while (true) {
        cout << "\nChoose operation:\n";
        cout << "1. Add\n";
        cout << "2. Subtract\n";
        cout << "3. Multiply\n";
        cout << "4. Divide\n";
        cout << "5. Exit\n";

        cout << "Enter choice (1-5): ";
        cin >> choice;

        if (choice == 5) {
            cout << "Goodbye!\n";
            break;
        }

        if (choice < 1 || choice > 5) {
            cout << "Invalid choice. Try again.\n";
            continue;
        }

        cout << "Enter first number: ";
        cin >> num1;

        cout << "Enter second number: ";
        cin >> num2;

        double result;

        switch (choice) {
            case 1:
                result = num1 + num2;
                cout << "Result: " << result << endl;
                break;

            case 2:
                result = num1 - num2;
                cout << "Result: " << result << endl;
                break;

            case 3:
                result = num1 * num2;
                cout << "Result: " << result << endl;
                break;

            case 4:
                if (num2 == 0) {
                    cout << "Error: Cannot divide by zero\n";
                } else {
                    result = num1 / num2;
                    cout << "Result: " << result << endl;
                }
                break;

            default:
                cout << "Invalid input\n";
        }
    }

    return 0;
}
