#include <iostream>
#include <string>
using namespace std;

class Patient {
private:
    int patientID;
    string name;
    int age;
    string disease;

public:
    void addPatient() {
        cout << "Enter Patient ID: ";
        cin >> patientID;

        cin.ignore();

        cout << "Enter Patient Name: ";
        getline(cin, name);

        cout << "Enter Age: ";
        cin >> age;

        cin.ignore();

        cout << "Enter Disease: ";
        getline(cin, disease);
    }

    void displayPatient() {
        cout << "\n--- Patient Record ---" << endl;
        cout << "Patient ID : " << patientID << endl;
        cout << "Name       : " << name << endl;
        cout << "Age        : " << age << endl;
        cout << "Disease    : " << disease << endl;
    }
};

int main() {
    Patient p;

    cout << "=== Hospital Patient Record System ===" << endl;

    p.addPatient();
    p.displayPatient();

    return 0;
}

        
