#include <iostream>
#include <string>
using namespace std;

class Library {
private:
    int bookId;
    string bookName;
    string authorName;

public:
    void addBook() {
        cout << "Enter Book ID: ";
        cin >> bookId;
        cin.ignore();

        cout << "Enter Book Name: ";
        getline(cin, bookName);

        cout << "Enter Author Name: ";
        getline(cin, authorName);
    }

    void displayBook() {
        cout << "\nBook ID: " << bookId;
        cout << "\nBook Name: " << bookName;
        cout << "\nAuthor Name: " << authorName << endl;
    }
};

int main() {
    Library books[100];
    int choice, count = 0;

    do {
        cout << "\n===== LIBRARY MANAGEMENT SYSTEM =====";
        cout << "\n1. Add Book";
        cout << "\n2. Display All Books";
        cout << "\n3. Exit";
        cout << "\nEnter your choice
