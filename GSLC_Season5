#include <stdio.h>
#include <stdlib.h>

struct node {
    int data;
    struct node* next;
    struct node* prev;
};

struct node* head = NULL;
struct node* tail = NULL;

void insertAtBeginning(int data) {
    struct node* newNode = (struct node*)malloc(sizeof(struct node));
    newNode->data = data;
    newNode->next = head;
    newNode->prev = NULL;
    if (head != NULL) {
        head->prev = newNode;
    }
    head = newNode;
    if (tail == NULL) {
        tail = newNode;
    }
}

void deleteFromBeginning() {
    if (head == NULL) {
        printf("List is already empty.\n");
        return;
    }
    struct node* temp = head;
    head = head->next;
    if (head != NULL) {
        head->prev = NULL;
    }
    free(temp);
    if (head == NULL) {
        tail = NULL;
    }
}

void displayList() {
    if (head == NULL) {
        printf("List is empty.\n");
        return;
    }
    struct node* current = head;
    printf("List: ");
    while (current != NULL) {
        printf("%d ", current->data);
        current = current->next;
    }
    printf("\n");
}

int main() {
    while(1){
        system("cls");
        int pilih;
        int angka;
        displayList();
        printf("MENU\n");
        printf("1. Insert\n");
        printf("2. Delete\n");
        printf("3. Exit\n");
        printf("Choose : ");
        scanf("%d", &pilih);
        switch (pilih)
        {
        case 1:
            printf("Masukan angka yang akan dimasukan kedalam list : ");
            scanf("%d",&angka);
            insertAtBeginning(angka);
            break;
        case 2:
            deleteFromBeginning();
            break;
        case 3:
            exit(1);
        default:
            printf("\nSalah Input angka\n");
            getchar();getchar();
            break;
        }
    }
    return 0;
}
