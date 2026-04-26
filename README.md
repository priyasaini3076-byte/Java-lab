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

## assi-12
'''

class A extends Thread {
    public void run() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("A: " + i);
        }
    }
}

class B extends Thread {
    public void run() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("B: " + i);
        }
    }
}

class C extends Thread {
    public void run() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("C: " + i);
        }
    }
}

public class Main {
    public static void main(String[] args) {
        A a = new A();
        B b = new B();
        C c = new C();

        try {
            a.start();
            a.join();   // wait until A finishes

            b.start();
            b.join();   // wait until B finishes

            c.start();
            c.join();   // wait until C finishes

        } catch (InterruptedException e) {
            System.out.println(e);
        }
    }
}

'''

<img width="59" height="469" alt="image" src="https://github.com/user-attachments/assets/67d13dca-2903-45b6-b934-42e745ace91b" />
<img width="49" height="451" alt="image" src="https://github.com/user-attachments/assets/b4108c0d-14ce-4860-ae78-14177e6e374a" />
<img width="48" height="457" alt="image" src="https://github.com/user-attachments/assets/e191dcf3-e54f-46eb-9ac1-c9073e86b9d1" />
<img width="51" height="476" alt="image" src="https://github.com/user-attachments/assets/5c4810b8-d93f-4378-b860-3ae0eb6ab2eb" /> <img width="91" height="480" alt="image" src="https://github.com/user-attachments/assets/029559a1-db03-4904-8d09-9c5a58324cd6" />
<img width="78" height="385" alt="image" src="https://github.com/user-attachments/assets/1ef2adbf-ba12-4374-954a-d43d9b8433b3" />
<img width="51" height="481" alt="image" src="https://github.com/user-attachments/assets/cedca0a4-f3a8-4694-9d3e-4c6232f510a7" />
<img width="52" height="463" alt="image" src="https://github.com/user-attachments/assets/cfb8dce0-d4b8-4c4b-b03b-ae58725cf1e4" />
<img width="56" height="470" alt="image" src="https://github.com/user-attachments/assets/e153ce88-6a8e-40d4-9a64-adc42397ba42" />
<img width="53" height="471" alt="image" src="https://github.com/user-attachments/assets/f2f46a5a-7bc5-488f-a369-fa20e51a4580" />
<img width="49" height="481" alt="image" src="https://github.com/user-attachments/assets/f0bb0d72-35dc-4ffc-bfb6-2199016056e7" />
<img width="69" height="465" alt="image" src="https://github.com/user-attachments/assets/3150ded1-4398-4d39-a4ad-c1d4351d07ac" />
<img width="65" height="471" alt="image" src="https://github.com/user-attachments/assets/225c1faf-3afc-4b04-8e42-e8d4b7a0b3e9" />
<img width="58" height="476" alt="image" src="https://github.com/user-attachments/assets/3adb7be4-829a-4632-9697-e5382ec863c4" />
<img width="71" height="472" alt="image" src="https://github.com/user-attachments/assets/8b3120e4-efdf-4dce-b0d7-abb163d92f23" />
<img width="72" height="480" alt="image" src="https://github.com/user-attachments/assets/9af4d1c6-4532-4cf2-8e43-c1ac57a99d48" />

## assi-13
'''


import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter first number: ");
        int a = sc.nextInt();

        System.out.print("Enter second number: ");
        int b = sc.nextInt();

        int sum = a + b;

        System.out.println("Result: " + sum);
    }
}

'''

<img width="270" height="78" alt="image" src="https://github.com/user-attachments/assets/f754b4cb-67b6-4ab5-85e8-ce16aab863c1" />


## assi-14

'''

import java.util.*;

public class Main {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        // 🔹 Taking 10 inputs (Registration Form)
        System.out.print("Enter Name: ");
        String name = sc.nextLine();

        System.out.print("Enter Email: ");
        String email = sc.nextLine();

        System.out.print("Enter Password: ");
        String password = sc.nextLine();

        System.out.print("Enter Gender: ");
        String gender = sc.nextLine();

        System.out.print("Enter Course: ");
        String course = sc.nextLine();

        System.out.print("Enter Address: ");
        String address = sc.nextLine();

        System.out.print("Enter Phone: ");
        String phone = sc.nextLine();

        System.out.print("Enter Age: ");
        String age = sc.nextLine();

        System.out.print("Enter City: ");
        String city = sc.nextLine();

        System.out.print("Enter State: ");
        String state = sc.nextLine();

        // 🔹 Display Data (Simulating Database Storage)
        System.out.println("\n--- Registration Data ---");
        System.out.println("Name: " + name);
        System.out.println("Email: " + email);
        System.out.println("Password: " + password);
        System.out.println("Gender: " + gender);
        System.out.println("Course: " + course);
        System.out.println("Address: " + address);
        System.out.println("Phone: " + phone);
        System.out.println("Age: " + age);
        System.out.println("City: " + city);
        System.out.println("State: " + state);

        System.out.println("\nData Stored Successfully (Simulated)");
    }
}

'''

<img width="282" height="468" alt="image" src="https://github.com/user-attachments/assets/e1abaaf1-18e5-4939-b7bf-0dac061e0eff" />
<img width="343" height="147" alt="image" src="https://github.com/user-attachments/assets/d802f3c3-1e27-4fa4-b7ae-20f3e00c3018" />

## assi-15

'''


import javax.swing.*;
import java.awt.event.*;

public class Main {
    public static void main(String[] args) {

        JFrame f = new JFrame("Calculator");

        // Text fields
        JTextField t1 = new JTextField();
        JTextField t2 = new JTextField();
        JTextField result = new JTextField();

        // Buttons
        JButton add = new JButton("+");
        JButton sub = new JButton("-");
        JButton mul = new JButton("*");
        JButton div = new JButton("/");

        // Set positions
        t1.setBounds(50, 50, 150, 30);
        t2.setBounds(50, 100, 150, 30);
        result.setBounds(50, 150, 150, 30);

        add.setBounds(220, 50, 50, 30);
        sub.setBounds(280, 50, 50, 30);
        mul.setBounds(220, 100, 50, 30);
        div.setBounds(280, 100, 50, 30);

        // Action logic
        ActionListener al = new ActionListener() {
            public void actionPerformed(ActionEvent e) {
                try {
                    int a = Integer.parseInt(t1.getText());
                    int b = Integer.parseInt(t2.getText());
                    int res = 0;

                    if (e.getSource() == add) res = a + b;
                    if (e.getSource() == sub) res = a - b;
                    if (e.getSource() == mul) res = a * b;
                    if (e.getSource() == div) res = a / b;

                    result.setText(String.valueOf(res));

                } catch (Exception ex) {
                    JOptionPane.showMessageDialog(f, "Invalid Input");
                }
            }
        };

        // Add listeners
        add.addActionListener(al);
        sub.addActionListener(al);
        mul.addActionListener(al);
        div.addActionListener(al);

        // Add components
        f.add(t1); f.add(t2); f.add(result);
        f.add(add); f.add(sub); f.add(mul); f.add(div);

        // Frame settings
        f.setSize(400, 300);
        f.setLayout(null);
        f.setVisible(true);
        f.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
    }
}

'''

<img width="719" height="532" alt="image" src="https://github.com/user-attachments/assets/938ff50c-abda-4fd3-a23e-06b2a9c040bc" />

## assi-16

'''

import java.util.*;

public class Main {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        int[][] A = new int[2][2];
        int[][] B = new int[2][2];
        int[][] C = new int[2][2];

        System.out.println("Enter Matrix A:");
        for(int i=0;i<2;i++){
            for(int j=0;j<2;j++){
                A[i][j] = sc.nextInt();
            }
        }

        System.out.println("Enter Matrix B:");
        for(int i=0;i<2;i++){
            for(int j=0;j<2;j++){
                B[i][j] = sc.nextInt();
            }
        }

        // Addition
        for(int i=0;i<2;i++){
            for(int j=0;j<2;j++){
                C[i][j] = A[i][j] + B[i][j];
            }
        }

        System.out.println("Result Matrix:");
        for(int i=0;i<2;i++){
            for(int j=0;j<2;j++){
                System.out.print(C[i][j] + " ");
            }
            System.out.println();
        }
    }
}

'''

<img width="153" height="326" alt="image" src="https://github.com/user-attachments/assets/f06f9414-66ae-49d2-a183-da67a98a6a89" />


## assi-17

'''


import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

class DrawPanel extends JPanel {
    String shape = "";

    public void setShape(String s) {
        shape = s;
        repaint();
    }

    public void paintComponent(Graphics g) {
        super.paintComponent(g);

        if (shape.equals("Circle"))
            g.drawOval(150, 100, 100, 100);

        if (shape.equals("Oval"))
            g.drawOval(120, 100, 150, 80);

        if (shape.equals("Rectangle"))
            g.drawRect(120, 100, 150, 80);

        if (shape.equals("Square"))
            g.drawRect(150, 100, 100, 100);

        if (shape.equals("Line"))
            g.drawLine(100, 100, 250, 200);

        if (shape.equals("Triangle")) {
            int x[] = {150, 200, 250};
            int y[] = {200, 100, 200};
            g.drawPolygon(x, y, 3);
        }

        if (shape.equals("Arc"))
            g.drawArc(120, 100, 150, 100, 0, 180);

        if (shape.equals("RoundRect"))
            g.drawRoundRect(120, 100, 150, 80, 30, 30);

        if (shape.equals("Filled Circle"))
            g.fillOval(150, 100, 100, 100);

        if (shape.equals("Filled Rect"))
            g.fillRect(120, 100, 150, 80);
    }
}

public class Main {
    public static void main(String[] args) {

        JFrame f = new JFrame("Shapes using Buttons");
        f.setSize(500, 400);
        f.setLayout(null);

        DrawPanel panel = new DrawPanel();
        panel.setBounds(0, 100, 500, 300);

        String names[] = {
            "Circle", "Oval", "Rectangle", "Square", "Line",
            "Triangle", "Arc", "RoundRect", "Filled Circle", "Filled Rect"
        };

        int x = 10;

        for (int i = 0; i < 10; i++) {
            JButton btn = new JButton(names[i]);
            btn.setBounds(x, 10, 120, 30);
            x += 125;

            btn.addActionListener(new ActionListener() {
                public void actionPerformed(ActionEvent e) {
                    panel.setShape(((JButton)e.getSource()).getText());
                }
            });

            f.add(btn);
        }

        f.add(panel);

        f.setVisible(true);
        f.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
    }
}

'''
<img width="605" height="566" alt="image" src="https://github.com/user-attachments/assets/0b48f153-9257-456d-9405-56d06d9d0921" />

## assi-18

'''


import java.awt.*;
import java.awt.event.*;

public class PaintBrush extends Frame implements MouseListener, MouseMotionListener, ItemListener
{
    Choice colorChoice;
    Choice widthChoice;

    int x, y;
    Color currentColor = Color.BLACK;
    int brushSize = 5;

    public PaintBrush()
    {
        setTitle("Simple Paint Brush");
        setSize(600,500);
        setLayout(new FlowLayout());

        // Color Selection
        add(new Label("Select Color:"));
        colorChoice = new Choice();
        colorChoice.add("Black");
        colorChoice.add("Red");
        colorChoice.add("Blue");
        colorChoice.add("Green");
        add(colorChoice);

        // Width Selection
        add(new Label("Brush Width:"));
        widthChoice = new Choice();
        widthChoice.add("5");
        widthChoice.add("10");
        widthChoice.add("15");
        widthChoice.add("20");
        add(widthChoice);

        colorChoice.addItemListener(this);
        widthChoice.addItemListener(this);

        addMouseListener(this);
        addMouseMotionListener(this);

        // Closing Window
        addWindowListener(new WindowAdapter(){
            public void windowClosing(WindowEvent we){
                System.exit(0);
            }
        });

        setVisible(true);
    }

    public void itemStateChanged(ItemEvent e)
    {
        if(colorChoice.getSelectedItem().equals("Black"))
            currentColor = Color.BLACK;
        if(colorChoice.getSelectedItem().equals("Red"))
            currentColor = Color.RED;
        if(colorChoice.getSelectedItem().equals("Blue"))
            currentColor = Color.BLUE;
        if(colorChoice.getSelectedItem().equals("Green"))
            currentColor = Color.GREEN;

        brushSize = Integer.parseInt(widthChoice.getSelectedItem());
    }

    public void mousePressed(MouseEvent e)
    {
        x = e.getX();
        y = e.getY();
    }

    public void mouseDragged(MouseEvent e)
    {
        Graphics g = getGraphics();
        g.setColor(currentColor);
        g.fillOval(e.getX(), e.getY(), brushSize, brushSize);

        x = e.getX();
        y = e.getY();
    }

    // Required empty methods
    public void mouseClicked(MouseEvent e){}
    public void mouseReleased(MouseEvent e){}
    public void mouseEntered(MouseEvent e){}
    public void mouseExited(MouseEvent e){}
    public void mouseMoved(MouseEvent e){}

    public static void main(String args[])
    {
        new PaintBrush();
    }
}

'''

<img width="768" height="371" alt="image" src="https://github.com/user-attachments/assets/f48e4c3f-1b8f-4897-a84c-f390f4178d6f" />


## assi- 19

'''

class Add {
    void sum(int a, int b) {
        System.out.println("Sum = " + (a+b));
    }
}

class Subtract {
    void sub(int a, int b) {
        System.out.println("Difference = " + (a-b));
    }
}

class Multiply {
    void mul(int a, int b) {
        System.out.println("Product = " + (a*b));
    }
}

class Divide {
    void div(int a, int b) {
        System.out.println("Quotient = " + (a/b));
    }
}

class Modulus {
    void mod(int a, int b) {
        System.out.println("Remainder = " + (a%b));
    }
}

public class Main {
    public static void main(String args[]) {

        Add a = new Add();
        Subtract s = new Subtract();
        Multiply m = new Multiply();
        Divide d = new Divide();
        Modulus mo = new Modulus();

        a.sum(20,10);
        s.sub(20,10);
        m.mul(20,10);
        d.div(20,10);
        mo.mod(20,10);
    }
}

'''
<img width="163" height="128" alt="image" src="https://github.com/user-attachments/assets/b3bb96e4-7e05-4ecd-b58a-af5d57994519" />


## assi-20

'''

public class PackageDemo
{
    // Simulating package mypack
    static class Addition
    {
        void add(int a, int b)
        {
            System.out.println("Sum = " + (a+b));
        }
    }

    // Simulating subpackage mypack.subpack
    static class Multiply
    {
        void mul(int a, int b)
        {
            System.out.println("Product = " + (a*b));
        }
    }

    public static void main(String args[])
    {
        Addition obj1 = new Addition();
        Multiply obj2 = new Multiply();

        obj1.add(10,5);
        obj2.mul(10,5);
    }
}

'''

<img width="128" height="44" alt="image" src="https://github.com/user-attachments/assets/4dbd883f-12be-48d6-9d2d-c9d5cee6c252" />

## assi-21

'''

public class ExceptionDemo
{
    public static void main(String args[])
    {
        // Array Out of Bounds Exception
        try
        {
            int arr[] = {10,20,30,40,50};

            System.out.println("Array Elements:");
            for(int i=0;i<=5;i++) // causes exception
            {
                System.out.println(arr[i]);
            }
        }

        catch(ArrayIndexOutOfBoundsException e)
        {
            System.out.println("Error: Array index is out of bounds!");
        }


        // Arithmetic Exception
        try
        {
            int a=10, b=0;
            int c=a/b; // causes exception

            System.out.println("Result = " + c);
        }

        catch(ArithmeticException e)
        {
            System.out.println("Error: Division by zero is not allowed!");
        }
    }
}

'''

<img width="397" height="240" alt="image" src="https://github.com/user-attachments/assets/5b68e124-5c63-40bd-bcf4-199267af0d86" />

## assi-22

'''


import java.util.Scanner;

class InvalidAgeException extends Exception
{
   InvalidAgeException(String msg)
   {
       super(msg);
   }
}

public class StudentAgeTest
{
   public static void main(String args[])
   {
       Scanner sc = new Scanner(System.in);

       try
       {
           System.out.print("Enter student age: ");
           int age = sc.nextInt();

           if(age < 18 || age > 25)
           {
               throw new InvalidAgeException("Age must be between 18 and 25");
           }

           System.out.println("Valid Student Age");
       }

       catch(InvalidAgeException e)
       {
           System.out.println("Exception: " + e.getMessage());
       }
   }
}

'''

<img width="486" height="62" alt="image" src="https://github.com/user-attachments/assets/33e03b72-420e-4995-b341-d84c855b744f" />

## assi-23

'''

import java.io.*;

public class FileHandlingDemo
{
    public static void main(String args[]) throws Exception
    {
        // Writing into file
        FileWriter fw = new FileWriter("data.txt");
        fw.write("Hello Java");
        fw.close();

        // Character by Character Reading
        System.out.println("Character by Character:");
        FileReader fr = new FileReader("data.txt");

        int ch;
        while((ch = fr.read()) != -1)
        {
            System.out.print((char)ch);
        }
        fr.close();

        System.out.println();

        // Byte by Byte Reading
        System.out.println("Byte by Byte:");
        FileInputStream fin = new FileInputStream("data.txt");

        int b;
        while((b = fin.read()) != -1)
        {
            System.out.print((char)b);
        }
        fin.close();
    }
}

'''

<img width="270" height="146" alt="image" src="https://github.com/user-attachments/assets/c889e56c-6cb4-454d-a2af-a45727146f1c" />
