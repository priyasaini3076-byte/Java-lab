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

         
        
   
 













