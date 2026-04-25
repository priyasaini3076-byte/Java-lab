 [Program 1 WAP for arithmetic logic](#assi-1)

[Program 2 WAP for Hello World](#assi-2)

[Program-3 wap for the addition of two distances where each distance is given in meter,cm](#assi-3)

[Program-4 wap for the addition of two times where each time is given in hours , minutes](#assi-4)

[program-5 wap for the addtiton of two times where each time is given in hours, minutes and second](#assi-5)

[program-6 wap for the addition of two distances where each distance is given in meter ,cm and millimeter](#assi-6)

[prorgram-7 wap using objects and classes to do reverse of 1-D Array](#assi-7)

[program-8 write a class for implemenation operation of matrix 3*3: 1.Transpose, 2.Sum, 3.Multiply, 4.sum of row, 5. sum of column, 6.sum of diagonal](#assi-8)

[program-9 collect the code of C language for any 5 operation convert the logic to java in object orented fashion](#assi-9)

[program-10 Demostrate all three type of inheritance 1. single, 2.multilevel, 3.hierarchial](#assi-10)

[program-11 Write a program using three classes to print 1-100, 1-100, 1-100 with and without thread and analyse the output and repeat the same program using runnable interface](#assi-11)


[program-12 Using the concept of multithreading the output of all three threads must be synchronised (use join method)](#assi-12)


[program-13 Addition of 2 numbers using Swing](#assi-13)


[program-14 Make a registration form with 10 elements and send the data into database (use JDBC connectivity).](#assi-14)

[Program-15 Make one calculator in swing](#assi-15)

[Program-16 Matrix Addition using swing class](#assi-16)

[Program-17 Create one jframe apply 10 buttons on that after clicking on each button a new structure is created. (Circle, oval rectangle, etc](#assi-17)

[Program-18 Just using mouse Event create a frame like paint brush with selection of colour and width](#assi-18)

[Program-19 Create a package of any 5 classes of your choice and import it](#assi-19)

[Program-20 Create one package and sub package import and test it](#assi-20)

[Program-21 Create one small array of size 5 apply array out of bounds exception using try catch give a proper message in catch and demonstrate the exception exactly in the same fashion demonstrate arithmetic exception](#assi-21)

[Program-22 To test the range of age of one student.write a program using user defined exception](#assi-22)

[Program-23 File Handling Programs](#assi-23)

[Program-24 Inheritance Programs, using interface and abstract classes](#assi-24)






## assi-1

'''

 public class Cla{
 
static int add(int a, int b){

return a+b;

}

static int sub(int a, int b){

return a-b;

}

static int mul(int a, int b){

return a*b;

}

static int div(int a,int b){

return a/b;

}

public static void main(String[]args){

int n1=Integer.parseInt(args[0]);

int n2=Integer.parseInt(args[1]);

System.out.println(add(n1,n2)); 

System.out.println(sub(n1,n2));

System.out.println(mul(n1,n2)); 

System.out.println(div(n1,n2)); 

}

}
'''

<img width="423" height="117" alt="image" src="https://github.com/user-attachments/assets/82229e4f-e74c-4ee9-a9bd-1937d2d9ba52" />

## assi-2
'''

public class Add{

public static void main(String[]args)

{

System.out.println("Hi");

}

}
'''
<img width="105" height="39" alt="image" src="https://github.com/user-attachments/assets/f4933cd6-4986-4305-8041-ba9cf7937e6c" />


## assi-3

'''

import java.util.Scanner;

public class DistanceAddition {

    public static void main(String[] args) {
    
        Scanner sc = new Scanner(System.in);

        int m1, cm1, m2, cm2;
        
        int meter, cm;

        System.out.println("Enter first distance (meter and centimeter): ");
        
        m1 = sc.nextInt();
        
        cm1 = sc.nextInt();

        System.out.println("Enter second distance (meter and centimeter): ");
        
        m2 = sc.nextInt();
        
        cm2 = sc.nextInt();

        meter = m1 + m2;
        
        cm = cm1 + cm2;

        if (cm >= 100) {
        
            meter = meter + (cm / 100);
            
            cm = cm % 100;
        }

        System.out.println("Sum of distances = " + meter + " meter " + cm + " centimeter");
    }
    
}

'''
<img width="418" height="170" alt="image" src="https://github.com/user-attachments/assets/1927a594-24ca-40bd-bff8-5b5019211f39" />

## assi-4
'''

import java.util.Scanner;

class Time {

    int hours, minutes;

    void addTime(int h1, int m1, int h2, int m2) {
    
        hours = h1 + h2;

         minutes = m1 + m2;

        if (minutes >= 60) {
        
            hours = hours + minutes / 60;
            
            minutes = minutes % 60;
            
        }
        
    }

    void display() {
    
        System.out.println("Total Time = " + hours + " hours " + minutes + " minutes");
        
    }

    public static void main(String args[]) {
    
        Scanner sc = new Scanner(System.in);

        int h1, m1, h2, m2;

        System.out.print("Enter first time (hours minutes): ");
        
        h1 = sc.nextInt();
        
        m1 = sc.nextInt();

        System.out.print("Enter second time (hours minutes): ");
        
        h2 = sc.nextInt();
        
        m2 = sc.nextInt();

        Time t = new Time()
        
        t.addTime(h1, m1, h2, m2
        
        t.display();
        
    }
    
}

'''
<img width="359" height="120" alt="image" src="https://github.com/user-attachments/assets/143cc42d-fde5-4d72-b173-21b504d62af5" />

## assi-5
'''

import java.util.Scanner;

class Time {
    int hours, minutes, seconds;

    void addTime(int h1, int m1, int s1, int h2, int m2, int s2) {
        hours = h1 + h2;
        minutes = m1 + m2;
        seconds = s1 + s2;

        if (seconds >= 60) {
            minutes = minutes + seconds / 60;
            seconds = seconds % 60;
        }

        if (minutes >= 60) {
            hours = hours + minutes / 60;
            minutes = minutes % 60;
        }
    }

    void display() {
        System.out.println("Total Time = " + hours + " hours " + minutes + " minutes " + seconds + " seconds");
    }

    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);

        int h1, m1, s1, h2, m2, s2;

        System.out.print("Enter first time (hours minutes seconds): ");
        h1 = sc.nextInt();
        m1 = sc.nextInt();
        s1 = sc.nextInt();

        System.out.print("Enter second time (hours minutes seconds): ");
        h2 = sc.nextInt();
        m2 = sc.nextInt();
        s2 = sc.nextInt();

        Time t = new Time();   // object creation
        t.addTime(h1, m1, s1, h2, m2, s2);
        t.display();
    }
}

'''
<img width="424" height="200" alt="image" src="https://github.com/user-attachments/assets/b1de7738-3d92-4b60-bb6d-b4a8276d1c76" />

## assi-6
'''

import java.util.Scanner;

class Distance {
    int meter, centimeter, millimeter;

    void addDistance(int m1, int c1, int mm1, int m2, int c2, int mm2) {
        meter = m1 + m2;
        centimeter = c1 + c2;
        millimeter = mm1 + mm2;

        if (millimeter >= 10) {
            centimeter = centimeter + millimeter / 10;
            millimeter = millimeter % 10;
        }

        if (centimeter >= 100) {
            meter = meter + centimeter / 100;
            centimeter = centimeter % 100;
        }
    }

    void display() {
        System.out.println("Total Distance = " + meter + " meter " + centimeter + " centimeter " + millimeter + " millimeter");
    }

    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);

        int m1, c1, mm1, m2, c2, mm2;

        System.out.print("Enter first distance (meter centimeter millimeter): ");
        m1 = sc.nextInt();
        c1 = sc.nextInt();
        mm1 = sc.nextInt();

        System.out.print("Enter second distance (meter centimeter millimeter): ");
        m2 = sc.nextInt();
        c2 = sc.nextInt();
        mm2 = sc.nextInt();

        Distance d = new Distance();   // object creation
        d.addDistance(m1, c1, mm1, m2, c2, mm2);
        d.display();
    }
}
'''
<img width="548" height="197" alt="image" src="https://github.com/user-attachments/assets/4919e0d6-4fbf-4e9e-b5bd-6ab0f7ae13ec" />

## assi-7
'''

public class MainClass {

    public static void main(String[] args) {

        ArrayOperations obj = new ArrayOperations();

        System.out.println("Original Array:");
        
        obj.displayArray();

        obj.reverseArray();

        System.out.println("Reversed Array:");
        
        obj.displayArray();
    }
    
}

 class ArrayOperations {

    int[] arr = {10, 20, 30, 40, 50};  // predefined array

 void reverseArray() {
    
        int start = 0, end = arr.length - 1;

        while (start < end) {
        
            int temp = arr[start];
            
            arr[start] = arr[end];
            
            arr[end] = temp;

            start++;
            
            end--;
        }
        
    }

       void displayArray() {
       
        for(int i = 0; i < arr.length; i++) {
        
            System.out.print(arr[i] + " ");
            
        }
        
        System.out.println();

    }
    
}

'''
<img width="191" height="97" alt="image" src="https://github.com/user-attachments/assets/7db3c8d9-cfc6-4cd4-87cd-44605b9ac669" />

## assi-8
'''

public class MatrixOperations {

    int[][] A = {
        {1,2,3},
        {4,5,6},
        {7,8,9}
    };

    int[][] B = {
        {9,8,7},
        {6,5,4},
        {3,2,1}
    };

    void display(int[][] M){
        for(int i=0;i<3;i++){
            for(int j=0;j<3;j++){
                System.out.print(M[i][j]+" ");
            }
            System.out.println();
        }
    }

    void transpose(){
        int[][] T = new int[3][3];

        for(int i=0;i<3;i++){
            for(int j=0;j<3;j++){
                T[j][i] = A[i][j];
            }
        }

        System.out.println("Transpose of Matrix A:");
        display(T);
    }

    void sum(){
        int[][] S = new int[3][3];

        for(int i=0;i<3;i++){
            for(int j=0;j<3;j++){
                S[i][j] = A[i][j] + B[i][j];
            }
        }

        System.out.println("Sum of A and B:");
        display(S);
    }

    void multiply(){
        int[][] M = new int[3][3];

        for(int i=0;i<3;i++){
            for(int j=0;j<3;j++){
                for(int k=0;k<3;k++){
                    M[i][j] += A[i][k]*B[k][j];
                }
            }
        }

        System.out.println("Multiplication of A and B:");
        display(M);
    }

    void rowSum(){
        for(int i=0;i<3;i++){
            int sum=0;
            for(int j=0;j<3;j++){
                sum += A[i][j];
            }
            System.out.println("Row "+(i+1)+" Sum = "+sum);
        }
    }

    void columnSum(){
        for(int j=0;j<3;j++){
            int sum=0;
            for(int i=0;i<3;i++){
                sum += A[i][j];
            }
            System.out.println("Column "+(j+1)+" Sum = "+sum);
        }
    }

    void diagonalSum(){
        int p=0,s=0;

        for(int i=0;i<3;i++){
            p += A[i][i];
            s += A[i][2-i];
        }

        System.out.println("Primary Diagonal Sum = "+p);
        System.out.println("Secondary Diagonal Sum = "+s);
    }

    public static void main(String[] args){

        MatrixOperations obj = new MatrixOperations();

        System.out.println("Matrix A:");
        obj.display(obj.A);

        System.out.println("Matrix B:");
        obj.display(obj.B);

        obj.transpose();
        obj.sum();
        obj.multiply();
        obj.rowSum();
        obj.columnSum();
        obj.diagonalSum();
    }
}

'''

<img width="246" height="385" alt="image" src="https://github.com/user-attachments/assets/913d55f0-cd06-4211-9868-f83e4e0f4de6" />

<img width="282" height="295" alt="image" src="https://github.com/user-attachments/assets/509d7a86-abc7-43e0-8cb6-3ba6a5fa71d7" />


## assi-10

'''

// Base class
public class A {

    void showA() {
        System.out.println("Class A (Parent)");
    }

    public static void main(String[] args) {

        // Single Inheritance
        System.out.println("Single Inheritance:");
        B obj1 = new B();
        obj1.showA();
        obj1.showB();

        // Multilevel Inheritance
        System.out.println("\nMultilevel Inheritance:");
        C obj2 = new C();
        obj2.showA();
        obj2.showB();
        obj2.showC();

        // Hierarchical Inheritance
        System.out.println("\nHierarchical Inheritance:");
        D obj3 = new D();
        E obj4 = new E();

        obj3.showA();
        obj3.showD();

        obj4.showA();
        obj4.showE();
    }
}

// Single Inheritance
class B extends A {
    void showB() {
        System.out.println("Class B (Child of A)");
    }
}

// Multilevel Inheritance
class C extends B {
    void showC() {
        System.out.println("Class C (Child of B)");
    }
}

// Hierarchical Inheritance
class D extends A {
    void showD() {
        System.out.println("Class D (Another Child of A)");
    }
}

class E extends A {
    void showE() {
        System.out.println("Class E (Another Child of A)");
    }
}

 '''
 <img width="273" height="349" alt="image" src="https://github.com/user-attachments/assets/f6d41e4d-2c99-45b5-b40b-53c6c5584bae" />

 
## assi-11
'''


class A extends Thread {
    public void run() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("A (Thread): " + i);
        }
    }

    void print() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("A (Normal): " + i);
        }
    }
}

class B extends Thread {
    public void run() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("B (Thread): " + i);
        }
    }

    void print() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("B (Normal): " + i);
        }
    }
}

class C extends Thread {
    public void run() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("C (Thread): " + i);
        }
    }

    void print() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("C (Normal): " + i);
        }
    }
}

public class Main {
    public static void main(String[] args) {

        A a = new A();
        B b = new B();
        C c = new C();

        //  Without Thread (Sequential)
        System.out.println("----- WITHOUT THREAD -----");
        a.print();
        b.print();
        c.print();

        //  With Thread (Concurrent)
        System.out.println("----- WITH THREAD -----");
        a.start();
        b.start();
        c.start();
    }
}
'''

 <img width="176" height="474" alt="image" src="https://github.com/user-attachments/assets/723470d3-c192-404c-b5ae-a0506d965ca8" />
 <img width="182" height="458" alt="image" src="https://github.com/user-attachments/assets/3bb615a1-ef3e-4fe3-b5da-79a3661322a0" />
<img width="160" height="476" alt="image" src="https://github.com/user-attachments/assets/ec4eb265-f955-48af-8960-95df340f6fbd" />
<img width="150" height="459" alt="image" src="https://github.com/user-attachments/assets/cfd375fd-ea83-4b01-9329-b8fec3c0207b" />
<img width="168" height="476" alt="image" src="https://github.com/user-attachments/assets/8fa71e98-e3b8-472c-91ab-3a42ae44b742" />
<img width="200" height="477" alt="image" src="https://github.com/user-attachments/assets/0cb43fdb-0aba-4f76-800f-3e4568158c3f" />
<img width="158" height="478" alt="image" src="https://github.com/user-attachments/assets/488b174d-e820-4350-9113-4ebeee2ab56a" />
<img width="176" height="475" alt="image" src="https://github.com/user-attachments/assets/359af168-20c2-4d4d-a7b4-65eec211550c" />
<img width="147" height="477" alt="image" src="https://github.com/user-attachments/assets/21fb56d3-f331-40aa-9016-fa831bfe05cd" />
<img width="163" height="479" alt="image" src="https://github.com/user-attachments/assets/6ace8149-d68b-4abc-8661-1f1408d1b2a7" />
<img width="169" height="476" alt="image" src="https://github.com/user-attachments/assets/7a9af6e3-bb12-4662-ac95-b91710b42c54" />
<img width="168" height="478" alt="image" src="https://github.com/user-attachments/assets/ae3b014b-9eb3-4826-a2a4-8ce0029f6acd" />
<img width="135" height="458" alt="image" src="https://github.com/user-attachments/assets/2566556d-8e59-48ca-8868-d00482eee81a" />
<img width="139" height="471" alt="image" src="https://github.com/user-attachments/assets/8bda8b5a-c1c6-49a6-9175-f342d3d4b8b3" />
<img width="136" height="468" alt="image" src="https://github.com/user-attachments/assets/6635becd-0353-42f2-ac98-b4e573b8e6f7" />
<img width="145" height="457" alt="image" src="https://github.com/user-attachments/assets/842eda81-31b9-4abf-812a-6693e47fca95" />

