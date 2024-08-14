# Data Structures And Algorithms
This is my learning journey.
### 1) Arrays 
---
Init Array:
``` java
class Main{
    public static void main(String args[]){
        int arr[] = new int [sizeOfArray]; //init 1D Array
        int arr[][] = new int [][]; //init 2D Array
    }
}
```
Getting Input and Printing Output:
``` java
class Main{
    public static void main(String args[]){
       Scanner sc = new Scanner(System.in);
       int n = 10; //size of array;
       int arr[] = new int [n];
       for(int i = 0; i < n; i++){
           arr[i] = sc.nextInt(); //Input
       }
       for(int i = 0; i < n; i++){
           System.out.println(arr[i]); //printing the array values.
       }
    }
}
```
In 2D Array:
```java
class Main{
    public static void main(String args[]){
       Scanner sc = new Scanner(System.in);
       int n = 13; //row;
       int m =  3; //col
       int arr[][] = new int [n][m];
       for(int i = 0; i < arr.length; i++){
           for(int j = 0; j < arr[i].length; j++){
               arr[i][j] = sc.nextInt(); //getting input
           }
       }
       for(int i = 0; i < arr.length; i++){
           for(int j = 0; j < arr[i].length; j++){
              System.out.print(arr[i][j]); //printing
           }
       }
    }
}
```
### 2) ArrayList
---
``` java
import java.util.*;
class Main{
    public static void main(String args[]){
        ArrayList<Integer> arr = new ArrayList<Integer>(); //init arraylist
        arr.add(10); //Adding
        arr.set(0,33); //changing
        arr.remove(0); //removing
        arr.get(0); // accessing values
        arr.contains(5); //checking the value is present or not
    }
}
```
For 2D ArrayList:
``` java
import java.util.*;
class Main{
    public static void main(String args[]){
    ArrayList<ArrayList<Integer>> arr = new ArrayList<Integer>(); //init 2D ArrayList
    for(int i = 0; i < 3; i++){
        arr.add(new ArrayList<Integer>());
    }
    for(int i = 0; i < 3; i++){
        for(int j = 0; i < 3; i++){
            arr.get(i).add(2); //Adding
        }
    }
  }
}
```
---
### 3) LinkedList 
---
##### Insert at beginning:
Time Complexity:o(1)
``` java
class LinkedList{
    Node head;
    class Node{
        int data;
        Node next;
        Node(int val){
            data = val;
            next = null;
        }
    }
    LinkedList(){
        head = null;
    }
    void insertAtBeginning(int val){
        Node newNode = new Node(val);
        //when list is empty
        if(head == null){
            head = newNode;
        }
        //when list is not empty
        else{
            newNode.next = head;
            head = newNode;
        }
    }
    void display(){
        Node temp = head;
        while(temp != null){
            System.out.print(temp.data+" ");
            temp = temp.next;
        }
    }
}

class Main{
    public static void main(String args[]){
        LinkedList LL = new LinkedList();
        LL.insertAtBeginning(1);
        LL.insertAtBeginning(2);
        LL.insertAtBeginning(3);
        LL.insertAtBeginning(4);
        LL.insertAtBeginning(5);
        LL.insertAtBeginning(6);
        LL.display();
    }
}
```
##### Insert at Position:
Time Complexity:o(n)
``` java
void insertAtPos(int pos,int v){
        Node temp = head;
        if(pos == 0){
            insertAtBeginning(v);
            return;
        }
        Node newNode = new Node(v);
        for(int i = 0; i < pos-1; i++){
            temp = temp.next;
        }
        newNode.next = temp.next;
        temp.next = newNode;
    }
```
##### Delete at Position:
``` java
void delete(int p){
        Node temp = head;
        Node prev = null;
        for(int i=1;i<=p;i++){
            prev = temp;
            temp = temp.next;
        }
        prev.next = temp.next;
    }
```
##### Delete at Position:
``` java
 void reverse(){
        Node prev = null;
        Node curr = head;
        Node next = head.next;
        while(curr!=null){
            next = curr.next;
            curr.next = prev;
            prev = curr;
            curr = next;
        }
        head = prev;
    }
```
### 4) Doubly LinkedList 
---
##### Insert at beginning:
``` java
class LinkedList{
    Node head;
    class Node{
        int data;
        Node next;
        Node(int val){
            data = val;
            next = null;
        }
    }
    LinkedList(){
        head = null;
    }
    void insertAtBeginning(int val){
        Node newNode = new Node(val);
        //when list is empty
        if(head == null){
            head = newNode;
        }
        //when list is not empty
        else{
            newNode.next = head;
            head = newNode;
        }
    }
    void display(){
        Node temp = head;
        while(temp != null){
            System.out.print(temp.data+" ");
            temp = temp.next;
        }
    }
}

class Main{
    public static void main(String args[]){
        LinkedList LL = new LinkedList();
        LL.insertAtBeginning(1);
        LL.insertAtBeginning(2);
        LL.insertAtBeginning(3);
        LL.insertAtBeginning(4);
        LL.insertAtBeginning(5);
        LL.insertAtBeginning(6);
        LL.display();
    }
}
```
#### Display Reverse:
```java
void printRev(){
        Node temp = tail;
        while(temp!= null){
            System.out.print(temp.data+" -> ");
            temp = temp.prev;
        }
    }
```
