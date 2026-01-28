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


#6.  write a C++ program to print all elements to print all elements of  a matrix in column wise order 

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

    return 0;
}
<img width="523" height="324" alt="image" src="https://github.com/user-attachments/assets/950def07-5735-4efc-8079-6b237b6dd530" />

