# Linked List

## Linked Lists

## Introduction

- A linked list is a linear data structure.
- A linked list is an ordered collection of data elements where the order is given by means of links i.e. each element is connected or linked to another element.
- Nodes make up linked lists.
- Nodes are structures made up of data and a pointer to another node.
    
    ![](Linked%20List/imagesbe08c161-e81b-49e6-8c5c-7108c0532271-02_299_1385_1254_735.jpg)
    

HEAD

## Arrays Vs Linked Lists

| Arrays | Linked list |
| --- | --- |
| Fixed size: Resizing is expensive | Dynamic size |
| Insertions and Deletions are inefficient: Elements are usually shifted | Insertions and Deletions are efficient: No shifting |
| Random access i.e., efficient indexing | No random access- Not suitable for operations requiring accessing elements by index such as sorting |
| No memory waste if the array is full or almost full; otherwise may result in much memory waste. | Since memory is allocated dynamically(acc. to our need) there is no waste of memory. |
| Sequential access is faster [Reason: Elements in contiguous memory locations] | Sequential access is slow [Reason: Elements not in contiguous memory locations] |

## Types of Linked List

- There are four types of linked lists
1. Singly Linked list (SLL)
2. Doubly linked list (DLL)
3. Singly Circular Linked list (SCLL)
4. Doubly Circular linked list (DCLL)

## Singly Linked List

- Each node has only one link part.
- Each link part contains the address of the next node in the list.
- Link part of the last node contains NULL value which signifies the end of the node.

![](Linked%20List/imagesbe08c161-e81b-49e6-8c5c-7108c0532271-05_491_1591_941_757.jpg)

## Singly Linked List

Advantages:

1. Insertions and Deletions can be done easily.
2. It does not need movement of elements for insertion and deletion.
3. Its space is not wasted as we can get space according to our requirements.
4. Its size is not fixed.
5. It can be extended or reduced according to requirements.
6. Elements may or may not be stored in consecutive memory available, even then we can store the data in computer.
7. It is less expensive.

Disadvantages:

1. It requires more space as pointers are also stored with information.
2. Different amount of time is required to access each element.
3. If we have to go to a particular element then we have to go through all those elements that come before that element.
4. We can not traverse it from last & only from the beginning.
5. It is not easy to sort the elements stored in the linear linked list.

## Basic Operations on a list

- Creating a List
- Display a list
- Searching an element in the list
- Inserting an element in a list
- Deleting an element from a list

## Creation of a node in SLL

struct node
{
int data;
struct node *next;
};
typedef struct node*  nodeptr;
nodeptr list=NULL ;

## Create function of SLL

```c
nodeptr create( nodeptr list)
{
int n,i;
nodeptr newnode,curr;
printf("How many elements:");
scanf("%d",&n);
for(i=1;i<=n;i++)
{
        newnode=(struct node *)malloc(sizeof(struct node));
        printf("Enter number : ");
        scanf("%d",&newnode->data);
        newnode->next=NULL;
        if(list==NULL)
        {list=curr=newnode;}
        else
        { curr->next=newnode;
            curr=newnode;
        }
}return list;
}
```

## Display SLL

void display(nodeptr list)

```c
nodeptr curr;
for(curr=list ; curr!=NULL ; curr=curr->next)
    printf("%d\n",curr->data);
```

## Search an element in SLL

```c
void search(nodeptr list)
{
nodeptr curr;
int i,r;
printf("\n\n\tEnter element to search:");
scanf("%d",&r);
for(i=1,curr=list ; curr!=NULL ; curr=curr->next,i++)
{
if(curr->data==r)
{
printf("\n\n\t%d found at %d position!!!",r,i);
return;
}
}
printf("\n\n\t%d not found!!!");
}
```

## Insert an element in SLL

There are 3 cases here:-

- Insertion of an element at the beginning
- Insertion of an element at the end
- Insertion of an element after a particular node

There are two steps to be followed while inserting element at the beginning

- Make the next pointer of the node point towards the first node of the list
- Make the start pointer point towards this new node

If the list is empty simply make the start pointer point towards the new node;

## Insert an element in SLL

![](Linked%20List/imagesbe08c161-e81b-49e6-8c5c-7108c0532271-13_1163_2699_359_222.jpg)

Insertion of element at any position

## Insert an element in SLL

| nodeptr add(nodeptr list) | if $\left(\operatorname{pos}_{=}=1\right)$ |
| --- | --- |
| { nodeptr newnode,curr=list; | { newnode->next=curr; |
| int i,pos; | list=newnode; |
| printf(” $n \backslash n \backslash \mathrm{tEnter}$ position:“); |  |
| scanf(“%d”,&pos); | return list; |
| newnode $=($ struct node $*)$ malloc $($ sizeof $($ struct node $))$; | } |
| printf(“number :”); | for(i=1,curr=list;i<pos-1&&curr->next!=NULL; |
| scanf(“%d”,&newnode->data); | i++,curr=curr->next); |
| newnode->next=NULL; | newnode->next=curr->next; |
| if(list==NULL) | curr->next=newnode; |
| { list=newnode; |  |
| return list; | return list; |
| } | } |

## Delete an element from SLL

There are three cases here:-

- Deleting the first node
- Deleting the last node
- Deleting the intermediate node

Deletion of last node

![](Linked%20List/imagesbe08c161-e81b-49e6-8c5c-7108c0532271-15_417_1473_532_1596.jpg)

![](Linked%20List/imagesbe08c161-e81b-49e6-8c5c-7108c0532271-15_88_790_966_288.jpg)

![](Linked%20List/imagesbe08c161-e81b-49e6-8c5c-7108c0532271-15_571_3009_1119_189.jpg)

## Delete an element from SLL

```c
nodeptr del(nodeptr list) for(i=1,curr=list; i<pos-1 && curr->next!=NULL
for(i=1,curr=list; i<pos-1 && curr->next!=NULL
{
; i++,curr=curr->next);
nodeptr curr=list curr1. , 1++,cur-cur->nex),
int i,pos; if(curr->next==NULL)
if(curr->next==NULL)
printf("\n\n\tEnter position to delete:");
scanf("%d",&pos);
{ printf("\n\n\tPosition out of range");
if(list==NULL)
return list; }
{
    printf("\n\nList is empty"); return list;
curr1=curr->next;
}
curr->next=curr1->next;
if(pos==1)
{ list=curr->next;
free(curr1);
free(curr);
return list;
return list;
}
```

## Doubly Linked List

- Doubly linked list is a linked data structure that consists of a set of sequentially linked records called nodes.
- Each node contains three fields ::
    - One is data part which contain data only.
    - Two other field is links part that are point or references to the previous or to the next node in the sequence of nodes.
- The beginning and ending nodes’ previous and next links, respectively, point to some kind of terminator, typically a sentinel node or null to facilitate traversal of the list.

## Doubly Linked List

□ Advantages:
- We can traverse in both directions i.e. from starting to end and as well as from end to starting
- Some operations, such as deletion and inserting before a node, become easier
□ It is easy to reverse the linked list

- Disadvantages:
    - Requires more space
    □ List manipulations are slower (because more links must be changed)
    - Greater chance of having bugs (because more links must be manipulated)

## Structure of Doubly Linked List

```c
struct node
{
int data;
struct node*next;
struct node*prev; //holds the address of previous node
};
```

![](Linked%20List/imagesbe08c161-e81b-49e6-8c5c-7108c0532271-19_414_1544_1103_688.jpg)

## Create() of Doubly Linked List

| nodeptr create( nodeptr list) | if(list==NULL) |
| --- | --- |
| { |  |
| int n,i; | { list=curr=newnode; |
| nodeptr newnode,curr; | } |
| printf(“How many elements:”); | else |
| scanf(“%d”,&n); | { curr->next=newnode; |
| { | newnode->prev=curr; |
|  |  |
| newnode=(struct node | curr=newnode; |
| *)malloc(sizeof(struct node)); | } |
| printf(“Enter number :”); | }return list; |
| scanf(“%d”,&newnode->data); | } |
| newnode->next=newnode->prev=NULL; |  |

## Display DLL

void display(nodeptr list)

```c
nodeptr curr;
for(curr=list ; curr!=NULL ; curr=curr->next)
    printf("%d\n",curr->data);
```

## Search an element in DLL

```c
void search(nodeptr list)
{
nodeptr curr;
int i,r;
printf("\n\n\tEnter element to search:");
scanf("%d",&r);
for(i=1,curr=list ; curr!=NULL ; curr=curr->next,i++)
{
if(curr->data==r)
{
printf("\n\n\t%d found at %d position!!!",r,i);
return;
}
}
printf("\n\n\t%d not found!!!",r);
}
```

## Insert an element in DLL

| nodeptr add(nodeptr list) | if( $\operatorname{pos}_{=}=1$ ) |
| --- | --- |
| { nodeptr newnode,curr=list; | { newnode->next=curr; |
| int i,pos; | curr->prev=newnode; |
| printf(” ${ }^{(4 \backslash n \backslash t E n t e r ~ p o s i t i o n: ") ; ~}$ | list=newnode; |
| scanf(“%d”,&pos); | return list; |
| newnode = (struct node *)malloc(sizeof(struct node)); | } |
| printf(“number :”); | for $(\mathrm{i}=1$, curr = list; i<pos-1&& curr->next!=NULL; |
| scanf(“%d”,&newnode->data); | i++,curr=curr->next); |
| newnode->next=newnode->prev=NULL; | newnode->next=curr->next; |
| if(list==NULL) | newnode->prev=curr; |
| { list=newnode; | curr->next->prev=newnode. |
| return list; | curr->next=newnode; |
| } | return list; |
|  | } |

## Delete an element from DLL

```c
nodeptr del(nodeptr list) for(i=1,curr=list; ;<pos-1 && curr->next!=NULL
for(i=1,curr=list ; i<pos-1 && curr->next!=NULL
{
; i++,curr=curr->next);
nodeptr curr=list,curr1; , 1++,curr=curr->next),
int i,pos;
if(curr->next==NULL)
printf("\n\n\tEnter position to delete:");
scanf("%d",&pos);
{ printf("\n\n\tPosition out of range");
if(list==NULL)
return list; }
{
curr1=curr->next;
        printf("\n\nList is empty"); return list; curr1=curr->next;
}
if(pos==1)
curr->next=curr1->next;
{ list=curr->next;
curr1->next->prev=curr;
    curr->next->prev=curr->prev;
free(curr);
free(curr1);
return list;
return list;
}
    }
```

## Circular Linked List

- There are two types of circular linked list:
1. Singly Circular Linked List
2. Doubly Circular Linked List
- Advantages of circular linked list:
1. If we are at a node, then we can go to any node. But in singly linked list it is not possible to go to previous node.
2. It saves time when we have to go to the first node from the last node. It can be done in single step because there is no need to traverse the in between nodes. But in double linked list, we will have to go through in between nodes.
- Disadvantages of circular linked list:
1. It is not easy to reverse the linked list.
2. If proper care is not taken, then the problem of infinite loop can occur.
3. If we at a node and go back to the previous node, then we can not do it in single step. Instead, we have to complete the entire circle by going through the in between nodes and then we will reach the required node.

## Singly Circular Linked List

- Each node contains two fields like SLL
- One is data part which contain data only.
- Other field is the next node

![](Linked%20List/imagesbe08c161-e81b-49e6-8c5c-7108c0532271-26_192_1884_982_688.jpg)

## Create() of Singly Circular Linked List

| nodeptr create( nodeptr list) | if(list==NULL) |
| --- | --- |
| { { |  |
| int n,i; | list=curr=newnode; |
| nodeptr newnode,curr; | newnode->next=list; |
| printf(“How many elements:”); | } |
|  | else |
| for(i=1;i<=n;i++) | { curr->next=newnode; |
| newnode=(struct node *)malloc(sizeof(struct node)); printf(“Enter number :”); scanf(“%d”,&newnode->data); newnode->next=NULL; | newnode->next=list; curr=newnode; } }return list; |

## Display SCLL

```c
void display(nodeptr list)
    nodeptr curr;
    for(curr=list ; curr->next!=list ; curr=curr->next)
    {
        printf("%%d\n",curr->data);
    }
    printf("%d\n",curr->data);//last element
```

## Search an element in SCLL

```c
void search(nodeptr list)
        if(curr->data===r)//last element
        if(curr->data==r)//last element
{
        {
nodeptr curr;
        printf("\n\n\t%d found at %d position!!!",r,i);
int i,r;
        return;
printf("\n\n\tEnter element to search:");
        }
scanf("%d",&r);
        printf("\n\n\t%d not found!!!",r);
for(i=1,curr=list ; curr->next!=list ; curr=curr->next,i++)
        }
{
    if(curr->data==r) {
    printf("\n\n\t%d found at %d position!!!",r,i);
    return; }
}
```

## Insert an element in SCLL

| nodeptr add(nodeptr list) | if $(\operatorname{pos}==1)$ |
| --- | --- |
| { nodeptr newnode,curr=list; | { newnode->next=curr; |
| int i,pos; | for(curr=list;curr->next!=list;curr=curr->next); |
| printf(“’nposition:”); | list=newnode; |
| scanf(“%d”,&pos); | curr->next=list; |
| newnode $=($ struct node $*)$ malloc $($ sizeof $($ struct node $))$; | return list; |
| printf(“number :”); | } |
| scanf(“%d”,&newnode->data); | for $(\mathrm{i}=1$, curr = list; i<pos-1&&curr->next!=list; |
| newnode->next=NULL; | i++,curr=curr->next); |
| if(list==NULL) | newnode->next=curr->next; |
| { list=newnode; | curr->next=newnode; |
| newnode->next=list; | return list; |
| return list; | } |
| } |  |

## Delete an element from SCLL

```c
nodeptr del(nodeptr list)
{
nodeptr curr=list,curr1;
int i,pos;
printf("\n\n\tEnter position to delete:");
scanf("%d",&pos);
if(list==NULL)
{
    printf("\n\nList is empty"); return list;
}
if(pos==1)
{
curr=curr1=list;
for(curr=list;curr->next!=list;curr=curr->next);
curr->next=curr1->next;
list=curr1->next;
free(curr1);
return list;
}
```

```c
for(i=1,curr=list ; i<pos-1 && curr->next!=list;
i++,curr=curr->next);
if(curr->next==list)
{ printf("\n\n\tPosition out of range");
return list; }
curr1=curr->next;
curr->next=curr1->next;
free(curr1);
return list;
}
```