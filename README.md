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
### 1) Strings 
---
Init String:
``` java
public class Main
{
	public static void main(String[] args) {
		String a = "Hello World"; //store String
		System.out.print(a); //print String
	}
}
```
