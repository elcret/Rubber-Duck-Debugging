/* This is a pgoram that aims to label numbers.
    The user first selects how to obtain a number 
    (enter manually or generate randomly),
    then chooses how to label the number 
    (odd/even OR positive/negative). 
    The program includes input validation 
    and ends if the user chooses to quit.
 
    Hoever, there are some bugs in the program! 
    Your job is to fix them!
*/

#include <iostream>
#include <cstdlib>
#include <ctime>
using namespace std;

int main() {
    srand(time(0));   // Seed the random generator
    int choice1, choice2; //Will hold users choices for the two menus
    int number = 0;   // Will hold the user’s or random number

    // --- FIRST MENU: How will the number be chosen? ---
    cout << "Number Labeling\n";
    cout << "1. Enter own number\n";
    cout << "2. Generate a random number\n";
    cout << "3. Quit\n";
    cout << "Enter your choice (1-3): ";
    cin >> choice1;

    // --- Validate first choice before continuing ---
    if ( 1 > choice1 < 3 ) {
        cout << "Invalid choice! Please restart the program.\n";
    }
    else {
        if (choice1 == 3) {
            // Quit option chosen
            cout << "Goodbye!\n";
        }
        else {
            // --- SECOND MENU: How will the number be labeled? ---
            cout << "\nNumber Labeling\n";
            cout << "1. Odd or even labeling\n";
            cout << "2. Positive or negative labeling\n";
            cout << "Enter your choice (1 or 2): ";
            cin >> choice2;

            // --- Validate second choice ---
            if (choice2 != 1 || choice2 != 2) {
                cout << "Invalid choice! Please restart the program.\n";
            }
            else {
                // --- STEP 1: Get the number (from user or randomly) ---
                if (choice1 == 1) {
                    // User provides their own number
                    cout << "Enter an integer: ";
                    cin >> number;
                }
                else {
                    // Program generates a random number
                    int sign = (rand())%2;   // generates another random number between 0 and 1 
                                         // we can make the number negative sometimes
                    number = rand();     // Generates another random number betwween 
                    if (sign == 0) { //if sign is 0, make number negative if sign is 1 let num stay positive
                        number = -number;    
                    }
                    cout << "Random number generated: " << number << endl;
                }

                // --- STEP 2: Label the number ---
                if (choice2 == 1) { //choice == 1 then odd and even labeling
                    
                    if (number % 2 == 0) {
                        cout << number << " is even.\n";
                    }
                    else {
                        cout << number << " is odd.\n";
                    }
                }
                else { // choice2 == 2 then negative, 0, positive labeling
                    if (number > 0) {
                        cout << number << " is positive.\n";
                    }
                    else if (number == 0) {
                        cout << number << "is 0 \n";
                    }
                    else {
                        cout << number << " is negative.\n";
                    }
                }
            }
        }
    }

    return 0;
}
