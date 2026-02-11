''' Write a C++ program to implement a singly linked list using struct for the node and dynamic memory allocation with new and delete. Implement the following operations:

Insertion of a node at the beginning

Insertion of a node at the end

Deletion of a node

Display the entire list
Use new to allocate memory for each node, and delete to free memory when deleting nodes.'''

  #include <iostream>

struct Node {
    int data;
    Node* next;
};

class LinkedList {
private:
    Node* head;

public:
    LinkedList() : head(nullptr) {}

    // Destructor to prevent memory leaks
    ~LinkedList() {
        Node* current = head;
        while (current != nullptr) {
            Node* nextNode = current->next;
            delete current;
            current = nextNode;
        }
    }

    void insertBeginning(int val) {
        Node* newNode = new Node{val, head};
        head = newNode;
        std::cout << "Added " << val << " to the start.\n";
    }

    void insertEnd(int val) {
        Node* newNode = new Node{val, nullptr};
        if (!head) {
            head = newNode;
        } else {
            Node* temp = head;
            while (temp->next) temp = temp->next;
            temp->next = newNode;
        }
        std::cout << "Added " << val << " to the end.\n";
    }

    void deleteValue(int val) {
        if (!head) return;

        if (head->data == val) {
            Node* temp = head;
            head = head->next;
            delete temp;
            std::cout << "Deleted " << val << ".\n";
            return;
        }

        Node* temp = head;
        while (temp->next && temp->next->data != val) {
            temp = temp->next;
        }

        if (temp->next) {
            Node* toDelete = temp->next;
            temp->next = temp->next->next;
            delete toDelete;
            std::cout << "Deleted " << val << ".\n";
        } else {
            std::cout << "Value " << val << " not found.\n";
        }
    }

    void display() {
        if (!head) {
            std::cout << "List is empty.\n";
            return;
        }
        Node* temp = head;
        std::cout << "Current List: ";
        while (temp) {
            std::cout << temp->data << " -> ";
            temp = temp->next;
        }
        std::cout << "NULL\n";
    }
};

int main() {
    LinkedList list;
    int choice, value;

    do {
        std::cout << "\n--- Linked List Menu ---\n";
        std::cout << "1. Insert at Beginning\n";
        std::cout << "2. Insert at End\n";
        std::cout << "3. Delete a Value\n";
        std::cout << "4. Display List\n";
        std::cout << "5. Exit\n";
        std::cout << "Enter choice: ";
        std::cin >> choice;

        switch (choice) {
            case 1:
                std::cout << "Enter value: ";
                std::cin >> value;
                list.insertBeginning(value);
                break;
            case 2:
                std::cout << "Enter value: ";
                std::cin >> value;
                list.insertEnd(value);
                break;
            case 3:
                std::cout << "Enter value to delete: ";
                std::cin >> value;
                list.deleteValue(value);
                break;
            case 4:
                list.display();
                break;
            case 5:
                std::cout << "Exiting program...\n";
                break;
            default:
                std::cout << "Invalid choice!\n";
        }
    } while (choice != 5);

    return 0;
}

<img width="511" height="288" alt="image" src="https://github.com/user-attachments/assets/64a03529-7fc8-43d1-93c8-dd18875f9672" />


  
