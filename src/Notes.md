## 1D Arrays

### ways to declare them:

Interger Arrays
```java
int[] myArray = new int[10];

int[] map; //decalred, but not initialized

int[] terrian;
terrian = new in[100];
```
Object Arrays
```java
String[] myString = new String[10];
Player[] players = new PLayer[100];
Student students[] = new Students[1000];
```

Array Initializers
```java
int a[] = {1,2,3,4,5,6,8};
```

### Accessing elements

```java
int a[] = new int[100];
String b[] = new String[100];
Student c[] = new Student[100];

//access the 20th element
int temp1 = a[20];
String temp2 = b[20];
Student temp3 = c[20];
```
- element start at 0 and go to length-1

Length of Array

```java
int a[] = new int[10];
String b[] = new String[100];
Student c[] = new Student[1000];

System.out.println(a.length);
System.out.println(b.length);
System.out.println(c.length);
```
- Output
```
10
100
1000
```

Replacing Array Elements

```java
int a[] = new int[10];
String b[] = new String[100];
Student c[] = new Student[1000];

//change the 5th element
a[5] = 10;
b[5] = "Hello";
c[5] = new Student("William Zhang");
```

### For loop through an Array
```java
int a[] = new int[10];

for(int i=0; i<a.length; i++){
    int temp = a[i]; //current element
}

//identical to loop above
for(int temp: a){

}
```

Two things to know about for-each looping
- there is no i...so you never know WHERE you are
- no changing the structure of the array

Example: find the highest GPA student in an array of Students

```java
public Student bestGPA(Student[] students){
    int max = 0;
    
    for(int i = 0; i<students.length; i++){
        Student temp=students[i];
        if(temp.getGpa()>students[max].getGpa()){
        max=i;
        }
    }    
    return students[max];    
}
```
Example: Do all students have above 2.0
```java
public boolean allAbove2(Student[] arr){
    for(int i = 0; i<arr.length; i++){
        if(arr[i].getGpa() < 2)
            return false;
    }
    return true;
}

// Or

public boolean allAbove2(Student[] arr){
    for(Student s : arr){
        if(s.getGpa() <2.0)
            return false;
    }
    return true;
}
```
## ArrayLists

Why have ArrayList
- When you don't know the size of the array needed

### Declaring ArrayLists
```java
ArrayList<Student> list = new ArrayList<>();
ArrayList<Student> list2 = new ArrayList<Student>();
List<Student> list3 = new ArrayList<>();
List<Student> list4 = new ArrayList<Student>();

//use wrapper classes to create
ArrayList<Integer> list = new ArrayList<>();
ArrayList<Double> list = new ArrayList<>();
ArrayList<Boolean> list = new ArrayList<>();
```
### Accessing Elements
```java
ArrayList<Student> list3 = new ArrayList<>();

//get the 7th student
Student temp = list3.get(7);
```
How many things are in the ArrayList
```java
ArrayList<Student> list3 = new ArrayList<>();

System.out.println(list3.size());
```
- Output
```java
???? The number of itms in the list
```
### Change the element in the ArrayList
```java
ArrayList<Student> list3 = new ArrayList<>();

//change student 3's name to "Jason"
list3.get(3).setName("Jason");