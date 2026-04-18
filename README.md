 [Program 1 WAP for arithmetic logic](#assi-1)

[Program 2 WAP for Hello World](#assi-2)

[Program-3 wap for the addition of two distances where each distance is given in meter,cm](#assi-3)

[Program-4 wap for the addition of two times where each time is given in hours , minutes](#assi-4)

[program-5 wap for the addtiton of two times where each time is given in hours, minutes and second](#assi-5)

[program-6 wap for the addition of two distances where each distance is given in meter ,cm and millimeter](#assi-6)

[prorgram-7 wap using objects and classes to do reverse of 1-D Array](#assi-7)

[program-8 write a class for implemenation operation of matrix 3*3: 1.Transpose, 2.Sum, 3.Multiply, 4.sum of row, 5. sum of column, 6.sum of diagonal](#assi-8)

[program-9 collect the code of C language for any 5 operation convert the logic to java in object orented fashion](#assi-9)

[program-10 Demostrate all three type of inheritance 1. single, 2.multilevel, 3.hierarchial](#assi-1-)


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




         
        
   
 













