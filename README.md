#include <iostream>
#include <cstdlib>
#include <ctime>
using namespace std;

int main() {
    srand(time(0));
    int secret = rand() % 100 + 1;
    int guess = 0;
    int attempts = 0;

    cout << "Welcome to the Number Guessing Game!" << endl;
    cout << "\nGuess the number between 1 to 100: " << endl;

    while (guess != secret) {
        cin >> guess;
        attempts++;
        if (guess < secret) {
            cout << "Too low, try again: " << endl;
        }
        else if (guess > secret) {
            cout << "Too high, try again: " << endl;
        }
        else{
            cout << "Congratulations! you guessed the number in " << attempts << " attempts!" << endl;
        }
    }

    return 0;
}
