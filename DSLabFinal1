#include <iostream>

using namespace std;


struct Node {
    int data;
    Node* next;

    Node(int value) : data(value), next(nullptr) {}
};


class LinkedList {
private:
    Node* head;

public:
    LinkedList() : head(nullptr) {}

   
    void insert(int value) {
        Node* newNode = new Node(value);
        if (!head) {
            head = newNode;
        } else {
            Node* current = head;
            while (current->next) {
                current = current->next;
            }
            current->next = newNode;
        }
    }

   
    void remove(int value) {
        Node* current = head;
        Node* prev = nullptr;

        while (current && current->data != value) {
            prev = current;
            current = current->next;
        }

        if (current) {
            if (prev) {
                prev->next = current->next;
            } else {
                head = current->next;
            }
            delete current;
        }
    }

    
    void display() {
        Node* current = head;
        while (current) {
            cout << current->data << " ";
            current = current->next;
        }
        cout << endl;
    }

    
    ~LinkedList() {
        Node* current = head;
        Node* nextNode = nullptr;
        while (current) {
            nextNode = current->next;
            delete current;
            current = nextNode;
        }
    }
};


int main() {
    LinkedList myList;

   
    myList.insert(1);
    myList.insert(2);
    myList.insert(3);

    
    cout << "Linked List: ";
    myList.display();

  
    myList.remove(2);

    
    cout << "Modified Linked List: ";
    myList.display();

    return 0;
}
