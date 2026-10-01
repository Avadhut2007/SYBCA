# Lab Assignments

- Lab 1 (13/07)
    - Q.1 Write C functions to accept and display array elements. Also write a function to count even and odd number of array elements.
        
        ```c
        #include<stdio.h>
        
        void accept(int arr[], int n){
            for(int i=0;i<n;i++){
                printf("Enter element %d: ",i+1);
                scanf("%d",&arr[i]);
            }
        }
        
        void display(int arr[], int n){
            printf("Array elements: ");
            for(int i=0;i<n;i++)
                printf("%d ",arr[i]);
            printf("\n");
        }
        
        void countevenodd(int arr[], int n){
            int even=0, odd=0;
            for(int i=0;i<n;i++){
                if(arr[i]%2==0) even++;
                else odd++;
            }
            printf("Even count: %d\n",even);
            printf("Odd count: %d\n",odd);
        }
        
        int main(){
            int n;
            printf("Enter size of array: ");
            scanf("%d",&n);
            int arr[n];
        
            accept(arr,n);
            display(arr,n);
            countevenodd(arr,n);
        
            return 0;
        }
        
        ```
        
    - Q.2 Write a C function to find sum and product of array elements.
        
        ```c
        #include<stdio.h>
        
        void accept(int arr[], int n){
            for(int i=0;i<n;i++){
                printf("Enter element %d: ",i+1);
                scanf("%d",&arr[i]);
            }
        }
        
        void sumAndProduct(int arr[], int n){
            int sum=0, product=1;
            for(int i=0;i<n;i++){
                sum += arr[i];
                product *= arr[i];
            }
            printf("Sum = %d\n", sum);
            printf("Product = %d\n", product);
        }
        
        int main(){
            int n;
            printf("Enter size of array: ");
            scanf("%d",&n);
            int arr[n];
        
            accept(arr,n);
            sumAndProduct(arr,n);
        
            return 0;
        }
        ```
        
    - Q.3 Write a C program to create a structure employee with empno, ename, department and salary as data members. Write accept and display functions to accept&display details of employee.
        
        ```c
        #include<stdio.h>
        
        struct employee{
            int empno;
            char ename[30];
            char department[30];
            float salary;
        };
        
        void accept(struct employee *e){
            printf("Enter employee number: ");
            scanf("%d",&e->empno);
            getchar();
        
            printf("Enter employee name: ");
            fgets(e->ename, sizeof(e->ename), stdin);
        
            printf("Enter department: ");
            fgets(e->department, sizeof(e->department), stdin);
        
            printf("Enter salary: ");
            scanf("%f",&e->salary);
        }
        
        void display(struct employee *e){
            printf("\n--- Employee Details ---\n");
            printf("Emp No: %d\n", e->empno);
            printf("Name: %s", e->ename);
            printf("Department: %s", e->department);
            printf("Salary: %.2f\n", e->salary);
        }
        
        int main(){
            struct employee e;
            accept(&e);
            display(&e);
            return 0;
        }
        
        ```
        
    - Q.4 Write a C program to create a structure actor with ano, aname, age and experience as data members. Accept and display actor details using pointer instance
        
        ```c
        #include<stdio.h>
        
        struct actor{
            int ano;
            char aname[30];
            int age;
            int experience;
        };
        
        void accept(struct actor *a){
            printf("Enter actor number: ");
            scanf("%d",&a->ano);
            getchar();
        
            printf("Enter actor name: ");
            fgets(a->aname, sizeof(a->aname), stdin);
        
            printf("Enter age: ");
            scanf("%d",&a->age);
        
            printf("Enter experience (years): ");
            scanf("%d",&a->experience);
        }
        
        void display(struct actor *a){
            printf("\n--- Actor Details ---\n");
            printf("Actor No: %d\n", a->ano);
            printf("Name: %s", a->aname);
            printf("Age: %d\n", a->age);
            printf("Experience: %d years\n", a->experience);
        }
        
        int main(){
            struct actor a1, *ptr;
            ptr = &a1;
        
            accept(ptr);
            display(ptr);
        
            return 0;
        }
        
        ```
        
    - Q.5 Write a C program to create a structure student with prn, sname, course and percentage as data members. Write accept and display functions to accept & display details of ‘n’ students.
        
        ```c
        #include<stdio.h>
        
        struct student{
            int prn;
            char sname[30];
            char course[30];
            float percentage;
        };
        
        void accept(struct student s[], int n){
            for(int i=0;i<n;i++){
                printf("\nEnter details of student %d\n", i+1);
        
                printf("PRN: ");
                scanf("%d",&s[i].prn);
                getchar();
        
                printf("Name: ");
                fgets(s[i].sname, sizeof(s[i].sname), stdin);
        
                printf("Course: ");
                fgets(s[i].course, sizeof(s[i].course), stdin);
        
                printf("Percentage: ");
                scanf("%f",&s[i].percentage);
            }
        }
        
        void display(struct student s[], int n){
            printf("\n--- Student Details ---\n");
            for(int i=0;i<n;i++){
                printf("\nStudent %d\n", i+1);
                printf("PRN: %d\n", s[i].prn);
                printf("Name: %s", s[i].sname);
                printf("Course: %s", s[i].course);
                printf("Percentage: %.2f\n", s[i].percentage);
            }
        }
        
        int main(){
            int n;
            printf("Enter number of students: ");
            scanf("%d",&n);
        
            struct student s[n];
        
            accept(s,n);
            display(s,n);
        
            return 0;
        }
        
        ```
        
- Lab 2 (20/07)
    - Q.1 Write a C program to create a structure book with book no, book name, publisher name, author name, and price as data members. Write accept and display functions to accept & display details of ‘n’ books.
        
        ```c
        #include <stdio.h>
        
        struct book
        {
            int bookno;
            char bookname[50];
            char publisher[50];
            char author[50];
            float price;
        };
        
        void accept(struct book b[], int n)
        {
            int i;
            for(i = 0; i < n; i++)
            {
                printf("\nEnter details of Book %d\n", i + 1);
        
                printf("Book No: ");
                scanf("%d", &b[i].bookno);
        
                printf("Book Name: ");
                scanf("%s", b[i].bookname);
        
                printf("Publisher Name: ");
                scanf("%s", b[i].publisher);
        
                printf("Author Name: ");
                scanf("%s", b[i].author);
        
                printf("Price: ");
                scanf("%f", &b[i].price);
            }
        }
        
        void display(struct book b[], int n)
        {
            int i;
            printf("\nBook Details:\n");
        
            for(i = 0; i < n; i++)
            {
                printf("\nBook %d\n", i + 1);
                printf("Book No: %d\n", b[i].bookno);
                printf("Book Name: %s\n", b[i].bookname);
                printf("Publisher: %s\n", b[i].publisher);
                printf("Author: %s\n", b[i].author);
                printf("Price: %.2f\n", b[i].price);
            }
        }
        
        int main()
        {
            int n;
            printf("Enter number of books: ");
            scanf("%d", &n);
        
            struct book b[n];
        
            accept(b, n);
            display(b, n);
        
            return 0;
        }
        
        ```
        
    - Q.2 Write a menu driven C program to perform following operations on singly linked list.
    i.	Create SLL
    ii.	Display SLL
    iii.	Search an element in SLL
    iv.	Insert an element in SLL
        
        ```c
        #include <stdio.h>
        #include <stdlib.h>
        
        struct node
        {
            int data;
            struct node *next;
        };
        
        typedef struct node *nodeptr;
        
        nodeptr create(nodeptr list)
        {
            nodeptr newnode, curr;
            int n, i;
        
            printf("Enter number of nodes: ");
            scanf("%d", &n);
        
            for(i = 1; i <= n; i++)
            {
                newnode = (nodeptr)malloc(sizeof(struct node));
        
                printf("Enter data: ");
                scanf("%d", &newnode->data);
        
                newnode->next = NULL;
        
                if(list == NULL)
                {
                    list = newnode;
                }
                else
                {
                    curr = list;
                    while(curr->next != NULL)
                        curr = curr->next;
        
                    curr->next = newnode;
                }
            }
        
            return list;
        }
        
        void display(nodeptr list)
        {
            nodeptr curr;
        
            if(list == NULL)
            {
                printf("List is Empty\n");
                return;
            }
        
            printf("Linked List : ");
        
            for(curr = list; curr != NULL; curr = curr->next)
            {
                printf("%d -> ", curr->data);
            }
        
            printf("NULL\n");
        }
        
        void search(nodeptr list)
        {
            nodeptr curr;
            int key, pos = 1;
        
            printf("Enter element to search: ");
            scanf("%d", &key);
        
            for(curr = list; curr != NULL; curr = curr->next)
            {
                if(curr->data == key)
                {
                    printf("Element found at position %d\n", pos);
                    return;
                }
                pos++;
            }
        
            printf("Element not found.\n");
        }
        
        nodeptr add(nodeptr list)
        {
            nodeptr newnode, curr;
        
            newnode = (nodeptr)malloc(sizeof(struct node));
        
            printf("Enter element to insert: ");
            scanf("%d", &newnode->data);
        
            newnode->next = NULL;
        
            if(list == NULL)
            {
                list = newnode;
            }
            else
            {
                curr = list;
                while(curr->next != NULL)
                    curr = curr->next;
        
                curr->next = newnode;
            }
        
            printf("Element inserted successfully.\n");
        
            return list;
        }
        
        int main()
        {
            int ch;
            nodeptr list = NULL;
        
            do
            {
                printf("\n----- MENU -----\n");
                printf("1. Create SLL\n");
                printf("2. Display SLL\n");
                printf("3. Search Element\n");
                printf("4. Insert Element\n");
                printf("0. Exit\n");
        
                printf("Enter your choice: ");
                scanf("%d", &ch);
        
                switch(ch)
                {
                    case 0:
                        printf("Program Ended.\n");
                        break;
        
                    case 1:
                        list = create(list);
                        break;
        
                    case 2:
                        display(list);
                        break;
        
                    case 3:
                        search(list);
                        break;
        
                    case 4:
                        list = add(list);
                        break;
        
                    default:
                        printf("Invalid Choice.\n");
                }
        
            } while(ch != 0);
        
            return 0;
        }
        
        ```
        
- Lab 3 (27/07)
    - Q.1 Write a menu driven C program to perform following operations on singly linked list.
    i.	Create SLL
    ii.	Display SLL
    iii.	Delete a number from specified position
        
        ```c
        #include <stdio.h>
        #include <stdlib.h>
        
        struct node
        {
            int data;
            struct node *next;
        };
        typedef struct node *nodeptr;
        
        nodeptr create(nodeptr list)
        {
            nodeptr newnode, curr;
            int n, i;
            printf("Enter number of nodes: ");
            scanf("%d", &n);
            for(i = 1; i <= n; i++)
            {
                newnode = (nodeptr)malloc(sizeof(struct node));
                printf("Enter data: ");
                scanf("%d", &newnode->data);
                newnode->next = NULL;
                if(list == NULL)
                {
                    list = newnode;
                }
                else
                {
                    curr = list;
                    while(curr->next != NULL)
                        curr = curr->next;
                    curr->next = newnode;
                }
            }
            return list;
        }
        
        void display(nodeptr list)
        {
            nodeptr curr;
            if(list == NULL)
            {
                printf("List is Empty\n");
                return;
            }
            printf("Linked List : ");
            for(curr = list; curr != NULL; curr = curr->next)
            {
                printf("%d -> ", curr->data);
            }
            printf("NULL\n");
        }
        
        nodeptr del(nodeptr list)
        {
            nodeptr curr, temp;
            int pos, i;
        
            if(list == NULL)
            {
                printf("List is Empty\n");
                return list;
            }
        
            printf("Enter position: ");
            scanf("%d", &pos);
        
            if(pos < 1)
            {
                printf("Invalid Position\n");
                return list;
            }
        
            if(pos == 1)
            {
                temp = list;
                list = list->next;
                free(temp);
                printf("Node Deleted\n");
                return list;
            }
        
            curr = list;
            for(i = 1; i < pos - 1 && curr != NULL; i++)
                curr = curr->next;
        
            if(curr == NULL || curr->next == NULL)
            {
                printf("Invalid Position\n");
                return list;
            }
        
            temp = curr->next;
            curr->next = temp->next;
            free(temp);
            printf("Node Deleted\n");
            return list;
        }
        
        int main()
        {
            int ch;
            nodeptr list = NULL;
            do
            {
                printf("\n1.Create");
                printf("\n2.Display");
                printf("\n3.Delete");
                printf("\n0.Exit");
                printf("\nEnter your choice: ");
                scanf("%d", &ch);
                switch(ch)
                {
                    case 0: exit(0);
                    case 1:
                        list = create(list);
                        break;
                    case 2:
                        display(list);
                        break;
                    case 3:
                        list = del(list);
                        break;
                    default:
                        printf("Invalid Choice");
                }
            } while(ch != 0);
            return 0;
        }
        
        ```
        
    - Q.2 Write a C program to create and display a singly linked list with student details as student name, age, program name and percentage. Also write a function to display topper student details.
        
        ```c
        #include <stdio.h>
        #include <stdlib.h>
        #include <string.h>
        
        struct Node {
            char name[50];
            int age;
            char program[50];
            float percentage;
            struct Node *next;
        };
        
        struct Node *head = NULL;
        
        void create(char name[], int age, char program[], float percentage) {
            struct Node *newNode = (struct Node*)malloc(sizeof(struct Node));
            strcpy(newNode->name, name);
            newNode->age = age;
            strcpy(newNode->program, program);
            newNode->percentage = percentage;
            newNode->next = NULL;
            if (head == NULL) {
                head = newNode;
            } else {
                struct Node *temp = head;
                while (temp->next != NULL)
                    temp = temp->next;
                temp->next = newNode;
            }
        }
        
        void display() {
            struct Node *temp = head;
            while (temp != NULL) {
                printf("Name: %s\n", temp->name);
                printf("Age: %d\n", temp->age);
                printf("Program: %s\n", temp->program);
                printf("Percentage: %.2f\n", temp->percentage);
                printf("------------------------\n");
                temp = temp->next;
            }
        }
        
        void showTopper() {
            if (head == NULL) {
                printf("List is empty\n");
                return;
            }
            struct Node *temp = head;
            struct Node *topper = head;
            while (temp != NULL) {
                if (temp->percentage > topper->percentage)
                    topper = temp;
                temp = temp->next;
            }
            printf("Topper -> Name: %s\n", topper->name);
            printf("Age: %d\n", topper->age);
            printf("Program: %s\n", topper->program);
            printf("Percentage: %.2f\n", topper->percentage);
        }
        
        int main() {
            int n;
            printf("Enter Number of Students: ");
            scanf("%d", &n);
            for (int i = 0; i < n; i++) {
                char name[50], program[50];
                int age;
                float percentage;
                printf("Enter Information of student %d\n", i + 1);
                printf("Enter name: ");
                scanf("%s", name);
                printf("Enter age: ");
                scanf("%d", &age);
                printf("Enter program: ");
                scanf("%s", program);
                printf("Enter percentage: ");
                scanf("%f", &percentage);
                create(name, age, program, percentage);
            }
            printf("\n--- Student List ---\n");
            display();
            printf("\n--- Topper ---\n");
            showTopper();
            return 0;
        }
        
        ```
        
    - Q.3 Write a C program to create and display a singly linked list with employee details as employee name, department name, experience and salary. Also write a function to display employee details containing minimum salary.
        
        ```c
        #include<stdio.h>
        #include<stdlib.h>
        
        typedef struct employee {
            char ename[20], dname[20];
            int exp;
            float sal;
            struct employee *next;
        } *nodeptr;
        
        nodeptr create(nodeptr list) {
            int n;
            nodeptr newnode, curr = list;
            printf("Enter number of employees : ");
            scanf("%d", &n);
            while (n--) {
                newnode = malloc(sizeof(*newnode));
                printf("\nEnter Name : "); scanf("%s", newnode->ename);
                printf("Enter Department : "); scanf("%s", newnode->dname);
                printf("Enter Experience : "); scanf("%d", &newnode->exp);
                printf("Enter Salary : "); scanf("%f", &newnode->sal);
                newnode->next = NULL;
                if (!list) list = curr = newnode;
                else { curr->next = newnode; curr = newnode; }
            }
            return list;
        }
        
        void display(nodeptr list) {
            for (; list; list = list->next)
                printf("\n%s\t%s\t%d\t%.2f", list->ename, list->dname, list->exp, list->sal);
        }
        
        void minsalary(nodeptr list) {
            nodeptr temp = list;
            for (nodeptr curr = list; curr; curr = curr->next)
                if (curr->sal < temp->sal) temp = curr;
            printf("\n\nEmployee with Minimum Salary\n%s\t%s\t%d\t%.2f",
                   temp->ename, temp->dname, temp->exp, temp->sal);
        }
        
        int main() {
            nodeptr list = create(NULL);
            display(list);
            minsalary(list);
            return 0;
        }
        ```
        
- Lab 4 (03/08)
    - Q.1 Write a menu driven C program to perform following operations on doubly linked list.
    i.	Create DLL
    ii.	Display DLL
    iii.	Search DLL
    iv.	Insert a number at specified position
    v.	Delete a number from specified position
        
        ```c
        #include <stdio.h>
        #include <stdlib.h>
        
        struct node
        {
            int data;
            struct node *prev, *next;
        };
        typedef struct node *nodeptr;
        
        nodeptr create(nodeptr list)
        {
            nodeptr newnode, curr;
            int n, i;
        
            printf("Enter number of nodes: ");
            scanf("%d", &n);
        
            for(i = 1; i <= n; i++)
            {
                newnode = (nodeptr)malloc(sizeof(struct node));
                printf("Enter data: ");
                scanf("%d", &newnode->data);
                newnode->prev = newnode->next = NULL;
        
                if(list == NULL)
                {
                    list = newnode;
                }
                else
                {
                    curr = list;
                    while(curr->next != NULL)
                        curr = curr->next;
                    curr->next = newnode;
                    newnode->prev = curr;
                }
            }
            return list;
        }
        
        void display(nodeptr list)
        {
            nodeptr curr;
            if(list == NULL)
            {
                printf("List is Empty\n");
                return;
            }
            printf("Doubly Linked List : ");
            for(curr = list; curr != NULL; curr = curr->next)
                printf("%d <-> ", curr->data);
            printf("NULL\n");
        }
        
        void search(nodeptr list)
        {
            nodeptr curr;
            int key, pos = 1;
        
            printf("Enter element to search: ");
            scanf("%d", &key);
        
            for(curr = list; curr != NULL; curr = curr->next)
            {
                if(curr->data == key)
                {
                    printf("Element found at position %d\n", pos);
                    return;
                }
                pos++;
            }
            printf("Element not found.\n");
        }
        
        nodeptr insert(nodeptr list)
        {
            nodeptr newnode, curr;
            int pos, i;
        
            newnode = (nodeptr)malloc(sizeof(struct node));
            printf("Enter element to insert: ");
            scanf("%d", &newnode->data);
        
            printf("Enter position: ");
            scanf("%d", &pos);
        
            newnode->prev = newnode->next = NULL;
        
            if(pos == 1 || list == NULL)
            {
                newnode->next = list;
                if(list != NULL)
                    list->prev = newnode;
                list = newnode;
                printf("Node Inserted\n");
                return list;
            }
        
            curr = list;
            for(i = 1; i < pos - 1 && curr->next != NULL; i++)
                curr = curr->next;
        
            newnode->next = curr->next;
            newnode->prev = curr;
            if(curr->next != NULL)
                curr->next->prev = newnode;
            curr->next = newnode;
        
            printf("Node Inserted\n");
            return list;
        }
        
        nodeptr del(nodeptr list)
        {
            nodeptr curr;
            int pos, i;
        
            if(list == NULL)
            {
                printf("List is Empty\n");
                return list;
            }
        
            printf("Enter position: ");
            scanf("%d", &pos);
        
            curr = list;
            for(i = 1; i < pos && curr != NULL; i++)
                curr = curr->next;
        
            if(curr == NULL)
            {
                printf("Invalid Position\n");
                return list;
            }
        
            if(curr->prev != NULL)
                curr->prev->next = curr->next;
            else
                list = curr->next;
        
            if(curr->next != NULL)
                curr->next->prev = curr->prev;
        
            free(curr);
            printf("Node Deleted\n");
            return list;
        }
        
        int main()
        {
            int ch;
            nodeptr list = NULL;
        
            do
            {
                printf("\n----- MENU -----\n");
                printf("1. Create DLL\n");
                printf("2. Display DLL\n");
                printf("3. Search DLL\n");
                printf("4. Insert at Position\n");
                printf("5. Delete from Position\n");
                printf("0. Exit\n");
                printf("Enter your choice: ");
                scanf("%d", &ch);
        
                switch(ch)
                {
                    case 0:
                        printf("Program Ended.\n");
                        break;
                    case 1:
                        list = create(list);
                        break;
                    case 2:
                        display(list);
                        break;
                    case 3:
                        search(list);
                        break;
                    case 4:
                        list = insert(list);
                        break;
                    case 5:
                        list = del(list);
                        break;
                    default:
                        printf("Invalid Choice.\n");
                }
            } while(ch != 0);
        
            return 0;
        }
        ```
        
        **Output:**
        
        ```
        1. Create DLL
        2. Display DLL
        3. Search DLL
        4. Insert at Position
        5. Delete from Position
        0. Exit
        Enter your choice: 1
        Enter number of nodes: 3
        Enter data: 10
        Enter data: 20
        Enter data: 30
        
        Enter your choice: 2
        Doubly Linked List : 10 <-> 20 <-> 30 <-> NULL
        
        Enter your choice: 4
        Enter element to insert: 15
        Enter position: 2
        Node Inserted
        
        Enter your choice: 2
        Doubly Linked List : 10 <-> 15 <-> 20 <-> 30 <-> NULL
        
        Enter your choice: 5
        Enter position: 1
        Node Deleted
        
        Enter your choice: 2
        Doubly Linked List : 15 <-> 20 <-> 30 <-> NULL
        
        Enter your choice: 0
        Program Ended.
        ```
        
    - Q.2 Write a C program to accept and display details of faculty members with faculty name, department, year of experience and salary using doubly linked list.
        
        ```c
        #include <stdio.h>
        #include <stdlib.h>
        
        struct node
        {
            char name[20], dept[20];
            float exp, salary;
            struct node *prev, *next;
        };
        typedef struct node *nodeptr;
        
        nodeptr create(nodeptr list)
        {
            int n, i;
            nodeptr newnode, curr;
        
            printf("Enter number of faculty: ");
            scanf("%d", &n);
        
            for(i = 1; i <= n; i++)
            {
                newnode = (nodeptr)malloc(sizeof(struct node));
        
                printf("\nEnter Name: ");
                scanf("%s", newnode->name);
        
                printf("Enter Department: ");
                scanf("%s", newnode->dept);
        
                printf("Enter Experience (years): ");
                scanf("%f", &newnode->exp);
        
                printf("Enter Salary: ");
                scanf("%f", &newnode->salary);
        
                newnode->prev = newnode->next = NULL;
        
                if(list == NULL)
                {
                    list = newnode;
                }
                else
                {
                    curr = list;
                    while(curr->next != NULL)
                        curr = curr->next;
                    curr->next = newnode;
                    newnode->prev = curr;
                }
            }
            return list;
        }
        
        void display(nodeptr list)
        {
            nodeptr curr;
            printf("\nFaculty Details:\n");
            for(curr = list; curr != NULL; curr = curr->next)
            {
                printf("\nName: %s", curr->name);
                printf("\nDepartment: %s", curr->dept);
                printf("\nExperience: %.1f years", curr->exp);
                printf("\nSalary: %.2f\n", curr->salary);
            }
        }
        
        int main()
        {
            nodeptr list = NULL;
        
            list = create(list);
            display(list);
        
            return 0;
        }
        ```
        
        **Output:**
        
        ```
        Enter number of faculty: 2
        
        Enter Name: Rahul
        Enter Department: CS
        Enter Experience (years): 5
        Enter Salary: 60000
        
        Enter Name: Priya
        Enter Department: IT
        Enter Experience (years): 3
        Enter Salary: 50000
        
        Faculty Details:
        
        Name: Rahul
        Department: CS
        Experience: 5.0 years
        Salary: 60000.00
        
        Name: Priya
        Department: IT
        Experience: 3.0 years
        Salary: 50000.00
        ```
        
- Lab 5 (10/08)
    - Q.1 Write a menu driven C program to perform following operations on singly circular linked list.
    i.	Create SCLL
    ii.	Display SCLL
    iii.	Search a number in a SCLL
    iv.	Insert a number at specified position
    v.	Delete a number from specified position
        
        ```c
        #include<stdio.h>
        #include<stdlib.h>
        
        struct node{
            int data;
            struct node *next;
        };
        struct node *head=NULL;
        
        void create(){
            int n,i,x;
            struct node *t,*p;
            printf("Enter number of nodes: ");
            scanf("%d",&n);
            for(i=0;i<n;i++){
                printf("Enter data: ");
                scanf("%d",&x);
                t=(struct node*)malloc(sizeof(struct node));
                t->data=x;
                if(head==NULL){
                    head=t;
                    t->next=head;
                }else{
                    p=head;
                    while(p->next!=head)
                        p=p->next;
                    p->next=t;
                    t->next=head;
                }
            }
        }
        
        void display(){
            struct node *p=head;
            if(head==NULL){
                printf("List Empty\n");
                return;
            }
            do{
                printf("%d -> ",p->data);
                p=p->next;
            }while(p!=head);
            printf("(head)\n");
        }
        
        void search(){
            int key,pos=1;
            struct node *p=head;
            printf("Enter number to search: ");
            scanf("%d",&key);
            do{
                if(p->data==key){
                    printf("Found at position %d\n",pos);
                    return;
                }
                p=p->next;
                pos++;
            }while(p!=head);
            printf("Not found\n");
        }
        
        void insert(){
            int pos,i,x;
            struct node *t,*p;
            printf("Enter data: ");
            scanf("%d",&x);
            printf("Enter position: ");
            scanf("%d",&pos);
            t=(struct node*)malloc(sizeof(struct node));
            t->data=x;
            if(pos==1){
                p=head;
                while(p->next!=head)
                    p=p->next;
                t->next=head;
                head=t;
                p->next=head;
            }else{
                p=head;
                for(i=1;i<pos-1;i++)
                    p=p->next;
                t->next=p->next;
                p->next=t;
            }
            printf("Inserted\n");
        }
        
        void del(){
            int pos,i;
            struct node *p,*t;
            printf("Enter position: ");
            scanf("%d",&pos);
            if(pos==1){
                p=head;
                while(p->next!=head)
                    p=p->next;
                t=head;
                head=head->next;
                p->next=head;
                free(t);
            }else{
                p=head;
                for(i=1;i<pos-1;i++)
                    p=p->next;
                t=p->next;
                p->next=t->next;
                free(t);
            }
            printf("Deleted\n");
        }
        
        int main(){
            int ch;
            do{
                printf("\n1.Create 2.Display 3.Search 4.Insert 5.Delete 0.Exit\n");
                printf("Enter choice: ");
                scanf("%d",&ch);
                switch(ch){
                    case 1: create(); break;
                    case 2: display(); break;
                    case 3: search(); break;
                    case 4: insert(); break;
                    case 5: del(); break;
                    case 0: printf("Exit\n"); break;
                    default: printf("Invalid\n");
                }
            }while(ch!=0);
            return 0;
        }
        ```
        
        **Output:**
        
        ```
        1.Create 2.Display 3.Search 4.Insert 5.Delete 0.Exit
        Enter choice: 1
        Enter number of nodes: 3
        Enter data: 10
        Enter data: 20
        Enter data: 30
        
        Enter choice: 2
        10 -> 20 -> 30 -> (head)
        
        Enter choice: 3
        Enter number to search: 20
        Found at position 2
        
        Enter choice: 4
        Enter data: 25
        Enter position: 3
        Inserted
        
        Enter choice: 2
        10 -> 20 -> 25 -> 30 -> (head)
        
        Enter choice: 0
        Exit
        ```
        
    - Q.2 Write a C program to accept and display details of vehicle with vehicle name, vehicle type, company name and price using singly circular linked list. Also display vehicle details having price more than Rs. 2 Lacs.
        
        ```c
        #include <stdio.h>
        #include <stdlib.h>
        
        struct node
        {
            char vname[20], vtype[20], company[20];
            float price;
            struct node *next;
        };
        typedef struct node *nodeptr;
        
        nodeptr create(nodeptr list)
        {
            int n, i;
            nodeptr newnode, curr;
        
            printf("Enter number of vehicles: ");
            scanf("%d", &n);
        
            for(i = 1; i <= n; i++)
            {
                newnode = (nodeptr)malloc(sizeof(struct node));
        
                printf("\nEnter Vehicle Name: ");
                scanf("%s", newnode->vname);
        
                printf("Enter Vehicle Type: ");
                scanf("%s", newnode->vtype);
        
                printf("Enter Company Name: ");
                scanf("%s", newnode->company);
        
                printf("Enter Price: ");
                scanf("%f", &newnode->price);
        
                if(list == NULL)
                {
                    list = newnode;
                    newnode->next = list;
                }
                else
                {
                    curr = list;
                    while(curr->next != list)
                        curr = curr->next;
                    curr->next = newnode;
                    newnode->next = list;
                }
            }
            return list;
        }
        
        void display(nodeptr list)
        {
            nodeptr curr;
            if(list == NULL)
            {
                printf("List is Empty\n");
                return;
            }
            printf("\nVehicle Details:\n");
            curr = list;
            do
            {
                printf("\nName: %s", curr->vname);
                printf("\nType: %s", curr->vtype);
                printf("\nCompany: %s", curr->company);
                printf("\nPrice: %.2f\n", curr->price);
                curr = curr->next;
            } while(curr != list);
        }
        
        void displayAbove2Lacs(nodeptr list)
        {
            nodeptr curr;
            if(list == NULL)
                return;
        
            printf("\nVehicles with Price above Rs. 2,00,000:\n");
            curr = list;
            do
            {
                if(curr->price > 200000)
                {
                    printf("\nName: %s", curr->vname);
                    printf("\nType: %s", curr->vtype);
                    printf("\nCompany: %s", curr->company);
                    printf("\nPrice: %.2f\n", curr->price);
                }
                curr = curr->next;
            } while(curr != list);
        }
        
        int main()
        {
            nodeptr list = NULL;
        
            list = create(list);
            display(list);
            displayAbove2Lacs(list);
        
            return 0;
        }
        ```
        
        **Output:**
        
        ```
        Enter number of vehicles: 2
        
        Enter Vehicle Name: Swift
        Enter Vehicle Type: Hatchback
        Enter Company Name: Maruti
        Enter Price: 650000
        
        Enter Vehicle Name: Activa
        Enter Vehicle Type: Scooter
        Enter Company Name: Honda
        Enter Price: 80000
        
        Vehicle Details:
        
        Name: Swift
        Type: Hatchback
        Company: Maruti
        Price: 650000.00
        
        Name: Activa
        Type: Scooter
        Company: Honda
        Price: 80000.00
        
        Vehicles with Price above Rs. 2,00,000:
        
        Name: Swift
        Type: Hatchback
        Company: Maruti
        Price: 650000.00
        ```
        
- Lab 6 (24/08)
    - Q.1 Write a program for static implementation of stack.
        
        ```c
        #include <stdio.h>
        #define MAX 5
        
        struct Stack {
            int stack[MAX];
            int top;
        } s;
        
        void initStack() {
            s.top = -1;
        }
        
        int isEmpty() {
            if (s.top == -1)
                return 1;
            else
                return 0;
        }
        
        int isFull() {
            if (s.top == MAX - 1)
                return 1;
            else
                return 0;
        }
        
        void push() {
            int x;
        
            if (isFull())
                printf("Stack Overflow\n");
            else {
                printf("Enter element: ");
                scanf("%d", &x);
                s.top++;
                s.stack[s.top] = x;
            }
        }
        
        void pop() {
            if (isEmpty())
                printf("Stack Underflow\n");
            else {
                printf("Deleted: %d\n", s.stack[s.top]);
                s.top--;
            }
        }
        
        void display() {
            int i;
        
            if (isEmpty())
                printf("Stack is Empty\n");
            else {
                printf("Stack: ");
                for (i = s.top; i >= 0; i--)
                    printf("%d ", s.stack[i]);
            }
        }
        
        int main() {
            int ch;
        
            initStack();
        
            do {
                printf("\n\n1. Push");
                printf("\n2. Pop");
                printf("\n3. Display");
                printf("\n4. Exit");
                printf("\nEnter choice: ");
                scanf("%d", &ch);
                switch (ch)
                {
                    case 1:
                        push();
                        break;
        
                    case 2:
                        pop();
                        break;
        
                    case 3:
                        display();
                        break;
        
                    case 4:
                        printf("Exit");
                        break;
        
                    default:
                        printf("Invalid choice");
                }
        
            } while (ch != 4);
        
            return 0;
        }
        
        ```
        
        **Output:**
        
        ```jsx
        1. Push
        2. Pop
        3. Display
        4. Exit
        Enter choice: 1
        Enter element: 10
        
        1. Push
        2. Pop
        3. Display
        4. Exit
        Enter choice: 1
        Enter element: 20
        
        1. Push
        2. Pop
        3. Display
        4. Exit
        Enter choice: 1
        Enter element: 30
        
        1. Push
        2. Pop
        3. Display
        4. Exit
        Enter choice: 3
        Stack: 30 20 10 
        
        1. Push
        2. Pop
        3. Display
        4. Exit
        Enter choice: 2
        Deleted: 30
        
        1. Push
        2. Pop
        3. Display
        4. Exit
        Enter choice: 3
        Stack: 20 10 
        
        1. Push
        2. Pop
        3. Display
        4. Exit
        Enter choice: 4
        Exit
        ```
        
    - Q.2 Write a program to find reverse string using stack.
        
        ```c
        #include <stdio.h>
        #include <string.h>
        #define MAX 100
        
        struct Stack {
            char arr[MAX];
            int top;
        };
        
        void initStack(struct Stack *s) {
            s->top = -1;
        }
        
        int isEmpty(struct Stack *s) {
            return s->top == -1;
        }
        
        int isFull(struct Stack *s) {
            return s->top == MAX - 1;
        }
        
        void push(struct Stack *s, char ch) {
            if (!isFull(s))
                s->arr[++s->top] = ch;
        }
        
        char pop(struct Stack *s) {
            if (!isEmpty(s))
                return s->arr[s->top--];
            return '\0';
        }
        
        int main() {
            struct Stack s;
            char str[MAX];
            int i;
        
            initStack(&s);
        
            printf("Enter string: ");
            gets(str);
        
            for (i = 0; str[i] != '\0'; i++)
                push(&s, str[i]);
        
            printf("Reverse: ");
            while (!isEmpty(&s))
                printf("%c", pop(&s));
        
            return 0;
        }
        
        ```
        
        **Output:**
        
        ```jsx
        Enter string: hello world
        Reverse: dlrow olleh
        ```
        
    - Q.3 Write a program to check string is palindrome or not using stack.
        
        ```c
        #include <stdio.h>
        
        #define SIZE 100
        
        int main()
        {
            char stack[SIZE], str[SIZE];
            int top = -1;
            int i, flag = 1;
        
            printf("Enter string: ");
            scanf("%s", str);
        
            for(i = 0; str[i] != '\0'; i++)
            {
                top++;
                stack[top] = str[i];
            }
        
            for(i = 0; str[i] != '\0'; i++)
            {
                if(str[i] != stack[top])
                {
                    flag = 0;
                    break;
                }
        
                top--;
            }
        
            if(flag == 1)
                printf("String is Palindrome");
            else
                printf("String is Not Palindrome");
        
            return 0;
        }
        
        ```
        
        **Output:**
        
        ```jsx
        Enter string: madam
        String is Palindrome
        
        Enter string: hello
        String is Not Palindrome
        ```
        
    - Q.4 Write a program to check expression is fully parenthesize or not.
        
        ```c
        #include <stdio.h>
        
        #define SIZE 100
        
        int main()
        {
            char stack[SIZE], exp[SIZE];
            int top = -1;
            int i, count = 0;
        
            printf("Enter expression: ");
            scanf("%s", exp);
        
            for(i = 0; exp[i] != '\0'; i++)
            {
                if(exp[i] == '(')
                {
                    top++;
                    stack[top] = exp[i];
                }
        
                else if(exp[i] == ')')
                {
                    if(top == -1)
                    {
                        printf("Not Fully Parenthesized");
                        return 0;
                    }
        
                    top--;
                }
        
                else if(exp[i] == '+' || exp[i] == '-' ||
                        exp[i] == '*' || exp[i] == '/')
                {
                    count++;
                }
            }
        
            if(top == -1 && count > 0)
                printf("Expression is Fully Parenthesized");
            else
                printf("Expression is Not Fully Parenthesized");
        
            return 0;
        }
        
        ```
        
        **Output:**
        
        ```jsx
        Enter expression: (a+b)*(c-d)
        Expression is Fully Parenthesized
        
        Enter expression: a+b
        Expression is Fully Parenthesized
        ```
        
- Lab 7 (31/08)
    - Q.1 Write a program for dynamic implementation of stack.
        
        ```c
        //Dynamic implementation of stack using linked list
        #include<stdio.h>
        #include<stdlib.h>
        
        struct node
        {
          int data;
          struct node *next;
        };
        
        struct node *top=NULL;
        
        int isempty()
        {
        	if(top==NULL)
        		return 1;
        	else
        		return 0;
        }
        
        void push(int x)
        {
        	struct node *newnode;
        	newnode=(struct node*)malloc(sizeof(struct node));
        	newnode->data=x;
        	newnode->next=top;
        	top=newnode;
        }
        
        int pop()
        {
        	struct node *temp;
        	int x;
        	if(isempty()==1)
        	{
        		printf("\n\n\tStack is empty");
        		return -1;
        	}
        	else
        	{
        		x=top->data;
        		temp=top;
        		top=top->next;
        		free(temp);
        		return x;
        	}
        }
        
        void display()
        {
        	struct node *p=top;
        	if(isempty()==1)
        		printf("\n\n\tStack is empty");
        	else
        	{
        		printf("\n\n\tStack elements : ");
        		while(p!=NULL)
        		{
        			printf("%d  ",p->data);
        			p=p->next;
        		}
        	}
        }
        
        int main()
        {
        	int ch,x;
        	do
        	{
        		printf("\n\n\t1.Push\n\t2.Pop\n\t3.Display\n\t4.Exit");
        		printf("\n\n\tEnter choice : ");
        		scanf("%d",&ch);
        		switch(ch)
        		{
        			case 1: printf("\n\n\tEnter element : ");
        					scanf("%d",&x);
        					push(x);
        					break;
        
        			case 2: x=pop();
        					if(x!=-1)
        					printf("\n\n\tDeleted element : %d",x);
        					break;
        
        			case 3: display();
        					break;
        
        			case 4: break;
        
        			default:printf("\n\n\tInvalid choice");
        		}
        	}while(ch!=4);
        	return 0;
        }
        ```
        
        **Output:**
        
        ```jsx
        1.Push
        2.Pop
        3.Display
        4.Exit
        
        Enter choice : 1
        
        Enter element : 10
        
        1.Push
        2.Pop
        3.Display
        4.Exit
        
        Enter choice : 1
        
        Enter element : 20
        
        1.Push
        2.Pop
        3.Display
        4.Exit
        
        Enter choice : 3
        
        Stack elements : 20  10
        
        1.Push
        2.Pop
        3.Display
        4.Exit
        
        Enter choice : 2
        
        Deleted element : 20
        
        1.Push
        2.Pop
        3.Display
        4.Exit
        
        Enter choice : 4
        ```
        
    - Q.2 Write a program to convert infix expression to postfix expression.
        
        ```c
        //Conversion from Infix expression to postfix expression
        #include<stdio.h>
        #include<stdlib.h>
        #define MAX 10
        
        struct stack
        {
          int top;
          int data[MAX];
        }s;
        
        void initstack()
        {
        	s.top=-1;
        }
        
        int isempty()
        {
            if(s.top==-1)
                return 1;
            else
                return 0;
        }
        
        int isfull()
        {
        	if(s.top==MAX-1)
                return 1;
            else
                return 0;
        }
        
        void push(char ch)
        {
         if(isfull()==1)
         printf("\n\n\tStack is full");
         else
         {
          s.top++;
          s.data[s.top] = ch;
         }
        }
        
        char pop()
        {
         if(isempty()==1)
         {
         printf("\n\n\tStack is empty");
         return -1;
         }
         else
         return s.data[s.top--];
        }
        
        int priority(char ch)//Priority of operator
        {
         switch(ch)
         {
        	case '(' : return 0;
        	case '+' : case '-' : case '$' : return 1;
        	case '*' : case '/' : case '%' : return 2;
        	case '^' : return 3;
         }
         return -1;
        }
        
        void postfix(char in[20],char post[20])
        {
        	int i,j=0;
        	char ch;
        	initstack();
        	for(i=0 ; in[i]!='\0' ; i++)
        	{
        	  if(in[i]=='(')
        	  push(in[i]);
        	  else if((in[i]>='A' && in[i]<='Z') || (in[i]>='a' && in[i]<='z'))
        	  {
        	   post[j++] = in[i];
        	  }
        	  else if(in[i]=='+'||in[i]=='-'||in[i]=='$'|| in[i]=='*'||in[i]=='/'||in[i]=='%'||in[i]=='^')
        	  {
        	   while(priority(in[i]) <= priority(s.data[s.top]))
               {
                   post[j] = pop();
               }
        	   push(in[i]);
        	  }
        	  else if(in[i]==')')
        	  {
        	   while((ch=pop()) !='(')
               {
                   post[j++]=ch;
               }
        	  }
        	}//end of for
        
        	while(isempty()!=1)
            {
                post[j++]=pop();
            }
        	post[j]='\0';
        }
        
        int main()
        {
        	char in[20],post[20];
        	printf("\n\n\tEnter infix expression : ");
        	scanf("%s",in);
        	postfix(in,post);
        	printf("\n\n\tPostfix expression is :%s",post);
        	return 0;
        }
        ```
        
        **Output:**
        
        ```jsx
        
        Enter infix expression : (a+b)*(c-d)
        
        Postfix expression is :ab+cd-*
        ```
        
    - Q.3 Write a program to evaluate postfix expression.
        
        ```c
        //Evaluation of postfix expression
        #include<stdio.h>
        #include<stdlib.h>
        #include<math.h>
        #define MAX 10
        
        struct stack
        {
          int top;
          int data[MAX];
        }s;
        
        void initstack()
        {
        	s.top=-1;
        }
        
        int isempty()
        {
            if(s.top==-1)
                return 1;
            else
                return 0;
        }
        
        int isfull()
        {
        	if(s.top==MAX-1)
                return 1;
            else
                return 0;
        }
        
        void push(int x)
        {
         if(isfull()==1)
         printf("\n\n\tStack is full");
         else
         {
          s.top++;
          s.data[s.top] = x;
         }
        }
        
        int pop()
        {
         if(isempty()==1)
         {
         printf("\n\n\tStack is empty");
         return -1;
         }
         else
         return s.data[s.top--];
        }
        
        int evaluate(char post[20])
        {
        	int i,a,b,res;
        	for(i=0 ; post[i]!='\0' ; i++)
        	{
        	  if(post[i]>='0' && post[i]<='9')
        	  push(post[i]-'0');
        	  else
        	  {
        	   b=pop();
        	   a=pop();
        	   switch(post[i])
        	   {
        		case '+' : res=a+b; break;
        		case '-' : res=a-b; break;
        		case '*' : res=a*b; break;
        		case '/' : res=a/b; break;
        		case '^' : res=pow(a,b); break;
        	   }
        	   push(res);
        	  }
        	}
        	return pop();
        }
        
        int main()
        {
        	char post[20];
        	int result;
        	initstack();
        	printf("\n\n\tEnter postfix expression : ");
        	scanf("%s",post);
        	result=evaluate(post);
        	printf("\n\n\tResult = %d",result);
        	return 0;
        }
        ```
        
        **Output:**
        
        ```jsx
        
        Enter postfix expression : 231*+9-
        
        Result = -4
        ```
        
- Lab 8 (17/09)
    - Q.1 Write a program for static implementation of linear queue.
        
        ```c
        #include<stdio.h>
        #include<stdlib.h>
        
        struct node
        {
            int data;
            struct node *next;
        };
        
        typedef struct node * nodeptr;
        nodeptr front,rear;
        
        void initiqueue()
        {
            front=rear=NULL;
        }
        
        int isempty()
        {
            if(rear==NULL)
                return 1;
            else
                return 0;
        }
        
        void add()
        {
            nodeptr newnode;
            newnode=(struct node *)malloc(sizeof(struct node));
            newnode->next=NULL;
            printf("Enter number :");
            scanf("%d",&newnode->data);
        
            if(rear==NULL)
            {
                front=rear=newnode;
            }
            else
            {
                rear->next=newnode;
                rear=newnode;
            }
        }
        
        void del()
        {
            nodeptr curr=front;
        
            if(isempty()==1)
            {
                printf("Queue is empty!!");
            }
            else
            {
                printf("Deleted number is %d", curr->data);
                front = curr->next;
                free(curr);
        
                if(front==NULL)
                    rear=NULL;
            }
        }
        
        void display()
        {
            nodeptr curr;
        
            if(isempty()==1)
                printf("Queue is empty!!");
            else
            {
                for(curr=front ; curr!=NULL ; curr=curr->next)
                {
                    printf("%d ",curr->data);
                }
            }
        }
        
        int main()
        {
            int ch;
            initiqueue();
        
            do
            {
                printf("\n0.Exit");
                printf("\n1.Add");
                printf("\n2.Delete");
                printf("\n3.Display");
                printf("\nEnter your choice : ");
                scanf("%d",&ch);
        
                switch(ch)
                {
                    case 0 : exit(0);
        
                    case 1 : add();
                             break;
        
                    case 2 : del();
                             break;
        
                    case 3 : display();
                             break;
        
                    default : printf("Invalid choice!!!!");
                }
        
            }while(ch!=0);
        
            return 0;
        }
        
        ```
        
    - Q.2 Write a program for dynamic implementation of linear queue.
        
        ```c
        #include<stdio.h>
        #include<stdlib.h>
        
        struct node
        {
            int data;
            struct node *next;
        };
        
        typedef struct node * nodeptr;
        nodeptr front,rear;
        
        void initiqueue()
        {
            front=rear=NULL;
        }
        
        int isempty()
        {
            if(rear==NULL)
                return 1;
            else
                return 0;
        }
        
        void add()
        {
            nodeptr newnode;
            newnode=(struct node *)malloc(sizeof(struct node));
            newnode->next=NULL;
            printf("Enter number :");
            scanf("%d",&newnode->data);
        
            if(rear==NULL)
            {
                front=rear=newnode;
            }
            else
            {
                rear->next=newnode;
                rear=newnode;
            }
        }
        
        void del()
        {
            nodeptr curr=front;
        
            if(isempty()==1)
            {
                printf("Queue is empty!!");
            }
            else
            {
                printf("Deleted number is %d", curr->data);
                front = curr->next;
                free(curr);
        
                if(front==NULL)
                    rear=NULL;
            }
        }
        
        void display()
        {
            nodeptr curr;
        
            if(isempty()==1)
                printf("Queue is empty!!");
            else
            {
                for(curr=front ; curr!=NULL ; curr=curr->next)
                {
                    printf("%d ",curr->data);
                }
            }
        }
        
        int main()
        {
            int ch;
            initiqueue();
        
            do
            {
                printf("\n0.Exit");
                printf("\n1.Add");
                printf("\n2.Delete");
                printf("\n3.Display");
                printf("\nEnter your choice : ");
                scanf("%d",&ch);
        
                switch(ch)
                {
                    case 0 : exit(0);
        
                    case 1 : add();
                             break;
        
                    case 2 : del();
                             break;
        
                    case 3 : display();
                             break;
        
                    default : printf("Invalid choice!!!!");
                }
        
            }while(ch!=0);
        
            return 0;
        }
        
        ```