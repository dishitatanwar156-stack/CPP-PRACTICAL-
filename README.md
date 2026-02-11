# CPP-PRACTICAL-
# 1.  write a program to read and display elements of an array . 
#include <iostream>
using namespace std;

int main() {
    int n;
    int arr[100];

    cout << "Enter number of elements: ";
    cin >> n;

    cout << "Enter " << n << " elements:" << endl;
    for (int i = 0; i < n; i++) {
        cin >> arr[i];
    }

    cout << "Array elements are:" << endl;
    for (int i = 0; i < n; i++) {
        cout << arr[i] << " ";
    }

    return 0;
}
<img width="514" height="208" alt="image" src="https://github.com/user-attachments/assets/e901b0fc-45d8-4e82-9aec-92f832e138f4" />


# 2.  write a c++ program to find the sum all elements in an array , with user input 

#include <iostream>
using namespace std;

int main() {
    int n, sum = 0;
    int arr[100];

    cout << "Enter number of elements: ";
    cin >> n;

    cout << "Enter " << n << " elements:" << endl;
    for (int i = 0; i < n; i++) {
        cin >> arr[i];
        sum += arr[i];
    }

    cout << "Sum of all elements in the array = " << sum << endl;

    return 0;
}

<img width="467" height="209" alt="image" src="https://github.com/user-attachments/assets/6e7cb23e-6d8c-4e91-a297-75c1686e6b4a" />


#  3. write a c++ program to copy one array into another , all user input 

#include <iostream>
using namespace std;

int main() {
    int n;
    int arr1[100], arr2[100];

    cout << "Enter number of elements: ";
    cin >> n;

    cout << "Enter elements of first array:" << endl;
    for (int i = 0; i < n; i++) {
        cin >> arr1[i];
    }

    // Copying elements from arr1 to arr2
    for (int i = 0; i < n; i++) {
        arr2[i] = arr1[i];
    }

    cout << "Elements of second array after copying:" << endl;
    for (int i = 0; i < n; i++) {
        cout << arr2[i] << " ";
    }

    return 0;
}
<img width="399" height="218" alt="image" src="https://github.com/user-attachments/assets/1a375f9a-5540-43a5-acda-ba6f7c883444" />

#  4. write a c++ program to print array elements in an array at an even index positons 

#include <iostream>
using namespace std;

int main() {
    int n;
    int arr[100];

    cout << "Enter number of elements: ";
    cin >> n;

    cout << "Enter array elements:" << endl;
    for (int i = 0; i < n; i++) {
        cin >> arr[i];
    }

    cout << "Elements at even index positions:" << endl;
    for (int i = 0; i < n; i += 2) {
        cout << arr[i] << " ";
    }

    return 0;
}
<img width="442" height="231" alt="image" src="https://github.com/user-attachments/assets/0a696135-f3dc-482a-9876-552ef7ba86ab" />


#  5. write a program to read and display a 2d array (matrix). and print all elements of a matrix in row wise order 

#include <iostream>
using namespace std;

int main() {
    int rows, cols;
    int matrix[10][10];

    cout << "Enter number of rows: ";
    cin >> rows;
    cout << "Enter number of columns: ";
    cin >> cols;

    cout << "Enter elements of the matrix:" << endl;
    for (int i = 0; i < rows; i++) {
        for (int j = 0; j < cols; j++) {
            cin >> matrix[i][j];
        }
    }

    cout << "Matrix elements in row-wise order:" << endl;
    for (int i = 0; i < rows; i++) {
        for (int j = 0; j < cols; j++) {
            cout << matrix[i][j] << " ";
        }
        cout << endl;
    }

    return 0;
}
<img width="458" height="314" alt="image" src="https://github.com/user-attachments/assets/feae9989-89c3-4d3d-aa02-659ee91ca370" />


# 6.  write a C++ program to print all elements to print all elements of  a matrix in column wise order 

#include <iostream>
using namespace std;

int main() {
    int rows, cols;
    int matrix[10][10];

    cout << "Enter number of rows: ";
    cin >> rows;
    cout << "Enter number of columns: ";
    cin >> cols;

    cout << "Enter elements of the matrix:" << endl;
    for (int i = 0; i < rows; i++) {
        for (int j = 0; j < cols; j++) {
            cin >> matrix[i][j];
        }
    }

    cout << "Matrix elements in column-wise order:" << endl;
    for (int j = 0; j < cols; j++) {
        for (int i = 0; i < rows; i++) {
            cout << matrix[i][j] << " ";
        }
        cout << endl;
    }

}
<img width="523" height="324" alt="image" src="https://github.com/user-attachments/assets/950def07-5735-4efc-8079-6b237b6dd530" />


# 7. create a structure student with : roll number , name  , marks  . input details by user of 5 students and display students who scored more than 75 marks . 
    return 0;

    #include <iostream>
#include <string>
using namespace std;

struct Student {
    int roll;
    string name;
    float marks;
};

int main() {
    Student s[5];

    // Input details
    for (int i = 0; i < 5; i++) {
        cout << "\nEnter details of student " << i + 1 << endl;

        cout << "Roll number: ";
        cin >> s[i].roll;

        cin.ignore(); // clear buffer
        cout << "Name: ";
        getline(cin, s[i].name);

        cout << "Marks: ";
        cin >> s[i].marks;
    }

    // Display students with marks > 75
    cout << "\nStudents who scored more than 75 marks:\n";

    for (int i = 0; i < 5; i++) {
        if (s[i].marks > 75) {
            cout << "\nRoll Number: " << s[i].roll;
            cout << "\nName: " << s[i].name;
            cout << "\nMarks: " << s[i].marks << endl;
        }
    }

    return 0;
}

<img width="573" height="555" alt="image" src="https://github.com/user-attachments/assets/b44d5172-1da8-4eaf-9fb5-a31d13b08ec3" />

<img width="737" height="215" alt="image" src="https://github.com/user-attachments/assets/09677b88-7065-4eca-a08e-76e9746fcaa2" />


#more simpler code using functions in C++
#include <iostream>
using namespace std;

struct Student {
    int roll;
    char name[20];
    int marks;
};

int main() {
    Student s[5];

    // Input
    for (int i = 0; i < 5; i++) {
        cout << "\nEnter details of student " << i + 1 << endl;
        cout << "Roll number: ";
        cin >> s[i].roll;
        cout << "Name: ";
        cin >> s[i].name;
        cout << "Marks: ";
        cin >> s[i].marks;
    }

    // Output
    cout << "\nStudents who scored more than 75 marks:\n";

    for (int i = 0; i < 5; i++) {
        if (s[i].marks > 75) {
            cout << "\nRoll number: " << s[i].roll;
            cout << "\nName: " << s[i].name;
            cout << "\nMarks: " << s[i].marks << endl;
        }
    }

    return 0;
}


# 8.Define a structure Employee containing: employee ID, name, basic salary .Calculate and display gross salary (basic + 20% HRA + 10% DA).

#include <iostream>
using namespace std;

struct Employee {
    int id;
    char name[50];
    float basic;
};

int main() {
    int n;
    Employee e[100];   // fixed size array

    cout << "Enter number of employees: ";
    cin >> n;

    // Input loop
    for (int i = 0; i < n; i++) {
        cout << "\nEnter details of employee " << i + 1 << endl;

        cout << "Employee ID: ";
        cin >> e[i].id;

        cout << "Employee Name: ";
        cin >> e[i].name;

        cout << "Basic Salary: ";
        cin >> e[i].basic;
    }

    // Output loop
    cout << "\n--- Gross Salary Details ---\n";

    for (int i = 0; i < n; i++) {
        float hra = 0.20 * e[i].basic;
        float da  = 0.10 * e[i].basic;
        float gross = e[i].basic + hra + da;

        cout << "\nEmployee ID  : " << e[i].id;
        cout << "\nName         : " << e[i].name;
        cout << "\nGross Salary : " << gross << endl;
    }

    return 0;
}


execute this code before learning for exam 



