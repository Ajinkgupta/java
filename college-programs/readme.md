## 1  Program to check whether a number is prime or not (Program on selection and iteration control statements.)

```
public class PrimeCheck
{
public static void main(String args[])
{
int i,m=0,flag=0;
int n=3; 
m=n/2;
if (n==0 || n==1) { System.out.println(n+" is not prime number"); }
else
{
for(i=2;i<=m;i++)
{
if(n%i==0)
{
System.out.println(n+" is not prime number");
flag=1;
break;
} }
if(flag==0) { System.out.println(n+" is prime number"); }
}  }}

```

## 2 Program to check whether the number is palindrome or not. Accept input from keyboard. (Program to demonstrate various ways of accepting data through keyboard.)

```
class PalindromeCheck
{
public static void main(String args[])
{
int n, r, sum=0, temp;
n = Integer.parseInt(args[0]); // input from keyboard using Command Line Arguments
temp = n;
while(n>0)
{
r=n%10; //getting remainder
sum=(sum*10)+r;
n=n/10; //getting quotient
} // end of while
if (temp==sum) System.out.println("palindrome number ");
else System.out.println("not palindrome");
} // end of main function
} // end of class
```


## 3 Write a program to demonstrate user defined class and different types of variables.(Program on class and objects)


```

public class VariableExample
{
int myVariable; // Instance Variable
static int data = 30; // Static or Class Variable
public static void main(String args[])
{
int a = 100; // Local Variable
VariableExample obj = new VariableExample();

System.out.println("Value of instance variable myVariable: "+obj.myVariable);
System.out.println("Value of static variable data: "+VariableExample.data);
System.out.println("Value of local variable a: "+a);
}
}

```


## 4 Write a program to perform addition, subtraction and multiplication on two complex numbers. (Program on method and constructor overloading)

```
class Complex
{
float x, y;
Complex(){ x=0.0f;y=0.0f; }
Complex(float a) {x=y=a; }
Complex(float real, float imag){x=real; y=imag; }
void show() { System.out.println(x + " +j " + y); }
void sum(Complex c1,Complex c2)
{
x=c1.x+c2.x;
y=c1.y+c2.y;
}
void sub(Complex c1,Complex c2)
{
x=(c1.x)-(c2.x);
y=(c1.y)-(c2.y);
}
void mul(Complex c1,Complex c2)
{
x=(c1.x*c2.x)-(c1.y*c2.y);
y=(c1.x*c2.y)+(c1.y*c2.x);
}
}

class ConstOverload
{
public static void main (String args[])
{
Complex A=new Complex(4.4f,7.7f);
Complex B =new Complex(2.7f);
Complex C=new Complex();
C.sum(A,B);
C.show();
Complex D=new Complex();
D.sub(A,B);
D.show();
Complex E=new Complex();
E.mul(A,B);
E.show();
}
}
```


## 5 Write a program to perform addition of 2 matrices (Program on 2D array)


```
import java.util.Scanner;
class AddMatrix
{
public static void main(String args[])
{
int row, col,i,j;
Scanner in = new Scanner(System.in);
System.out.println("Enter the number of rows");
row = in.nextInt();
System.out.println("Enter the number columns");
col = in.nextInt();
int mat1[][] = new int[row][col];
int mat2[][] = new int[row][col];
int res[][] = new int[row][col];
System.out.println("Enter the elements of matrix1");
for ( i= 0 ; i < row ; i++ )
{
for ( j= 0 ; j < col ;j++ ) mat1[i][j] = in.nextInt();
System.out.println();
}
System.out.println("Enter the elements of matrix2");
for ( i= 0 ; i < row ; i++ )
{
for ( j= 0 ; j < col ;j++ ) mat2[i][j] = in.nextInt();
System.out.println();
}
for ( i= 0 ; i < row ; i++ )
for ( j= 0 ; j < col ;j++ ) res[i][j] = mat1[i][j] + mat2[i][j] ;
System.out.println("Sum of matrices:-");
for ( i= 0 ; i < row ; i++ )
{
for ( j= 0 ; j < col ;j++ ) System.out.print(res[i][j]+"\t");
System.out.println();
}
}
}
```


## 6 Write a program to implement any five String and StringBuffer Class functions ()

```
public class SMethods
{
public static void main(String args[])
{
/*The Java String toUpperCase() method converts this String into uppercase letter and String
toLowerCase() method into lowercase letter.*/
String s1="Sachin";
System.out.println(s1.toUpperCase());//SACHIN
System.out.println(s1.toLowerCase());//sachin
System.out.println(s1);//Sachin(no change in original)
// The String class trim() method eliminates white spaces before and after the String.
String s2=" Sachin ";
System.out.println(s2);// Sachin
System.out.println(s2.trim());//Sachin
/* The method startsWith() checks whether the String starts with the letters passed as arguments
and endsWith() method checks whether the String ends with the letters passed as arguments. */
String s3="Sachin";
System.out.println(s3.startsWith("Sa"));//true
System.out.println(s3.endsWith("n"));//true
// The String class charAt() method returns a character at specified index.
String s4="Sachin";
System.out.println(s4.charAt(0));//S
System.out.println(s4.charAt(3));//h
// The String class length() method returns length of the specified String.
String s5="Sachin";
System.out.println(s5.length());//6
}
}
```

6.2 
```
public class SBMethods
{
public static void main(String args[])
{
// The append() method concatenates the given argument with this String.
StringBuffer sb1=new StringBuffer("Hello ");
sb1.append("Java");//now original string is changed
System.out.println(sb1);//prints Hello Java
// The insert() method inserts the given String with this string at the given position.
StringBuffer sb2=new StringBuffer(" Java ");
sb2.insert(0,"Hello");//now original string is changed
System.out.println(sb2);//prints Hello Java
/* The delete() method of the StringBuffer class deletes the String from the specified
beginIndex to endIndex. */
StringBuffer sb3=new StringBuffer("Hello");
sb3.delete(1,3);
System.out.println(sb3);//prints Hlo
// The reverse() method of the StringBuilder class reverses the current String.
StringBuffer sb4=new StringBuffer("Hello");
sb4.reverse();
System.out.println(sb4);//prints olleH
/* The capacity() method of the StringBuffer class returns the current capacity of the buffer. The
default capacity of the buffer is 16. If the number of character increases from its current
capacity, it increases the capacity by (oldcapacity*2)+2. For example if your current capacity is
16, it will be (16*2)+2=34. */
StringBuffer sb5=new StringBuffer();
System.out.println(sb5.capacity());//default 16
sb.append("Hello");
System.out.println(sb5.capacity());//now 16
sb.append("java is my favourite language");
System.out.println(sb5.capacity());//now (16*2)+2=34 i.e (oldcapacity*2)+2
}
}
```

## 7 Write a program to perform display details of Teacher (Program to perform Single Inheritance)

```
class Staff
{
int code; String name, address;
Staff (int c, String n, String a) { code=c; name=n; address=a; }
void showdata()
{
System.out.println("code : " + code);
System.out.println("name : " + name);
System.out.println("code : " + address);
}
}
class Teacher extends Staff
{
String subject, publication;
Teacher( int c, String n, String a, String s, String p) {super(c, n, a); subject=s; publication=p;}
void showdata()
{
super.showdata();
System.out.println("subject : " + subject);
System.out.println("publication : " + publication);
}
}
class SIDemo
{
public static void main(String args[])
{
Teacher T=new Teacher(1001,"ASL","AIROLI","DTS","NIRALI");
T.showdata();
}}

```


## 8 Write a program to perform display details of Regular TypistWrite a program to perform display details of Regular Typist (Program to perform Multilevel Inheritance)


```
class Staff
{
int code; String name, address;
Staff (int c, String n, String a) { code=c; name=n; address=a; }
void showdata()
{
System.out.println("code : " + code);
System.out.println("name : " + name);
System.out.println("code : " + address);
}
}
class Typist extends Staff
{
int speed;
Typist(int c, String n, String a, int s) {super (c, n, a); speed=s;}
void showdata()
{
super.showdata();
System.out.println("speed : " + speed);
}}
class Regular extends Typist
{
int pay ;
Regular (int c, String n, String a, int s, int p) {super(c, n, a, s); pay=p;}
void showdata()
{
super.showdata();
System.out.println("pay : "+pay);
}}

Staff

Typist

Regular

class MLIDemo
{
public static void main(String args[])
{
Regular R=new Regular(2001,"PQR","PANVEL",30,1200);
R.showdata();
}
}
```


## 9 Write a program to display total marks obtained by student. (Program to implement multiple inheritance using interface)

```

class Student
{
int rn;
void getno(int r) {rn=r;}
void putno()
{
System.out.println("Roll No. : " + rn);
}
}
class Test extends Student
{
int sem1, sem2;
void getmarks( int s1,int s2){sem1=s1; sem2=s2;}
void putmarks()
{
System.out.println("Marks Obtained:");
System.out.println(" Semester 1:"+sem1);
System.out.println("Semester 2:"+sem2);
}}
interface Sports
{
int score=10;
void putscore();
}
class Result extends Test implements Sports
{
int total;
void display()

Student

Test

Result

Sports

{
total=sem1+sem2+score;
putno();
putmarks();
putscore();
System.out.println("Total Marks: "+ total);
}
public void putscore()
{ System.out.println("Sports Weight:" + score);}
}
class IDemo
{
public static void main (String args[])
{
Result R=new Result();
R.getno(1);
R.getmarks(1200,1000);
R.display();
}}
```


## 10 
### 10A. Write a program to demonstrate ArithmeticException

```
class AEDemo
{
public static void main(String args[])
{
try{
int num1=30, num2=0;
int output=num1/num2;
System.out.println ("Result = " +output);
}
catch(ArithmeticException e)
{ System.out.println ("Arithmetic Exception: You can't divide an integer by 0"); }
}
}
```
### 10B. Write a program to demonstrate ArrayIndexOutOfBounds Exception

```
class AIBEDemo
{
public static void main(String args[])
{
try
{
int a[]=new int[10];
//Array has only 10 elements
a[11] = 9;
}
catch(ArrayIndexOutOfBoundsException e)
{ System.out.println ("ArrayIndexOutOfBounds"); }
}
}
```

##  11 Program on User Defined Exceptions
### Problem Definition 1: Define custom exception to display an error message.


```
/* This is my Exception class, I have named it MyException, you can give any name,
just remember that it should extend Exception class */
class MyException extends Exception
{
String str1;
/* Constructor of custom exception class, throwing the exception to a string and then
displaying that string along with the message. */
MyException(String str2) { str1=str2; }
public String toString(){ return ("MyException Occurred: "+str1) ; }
}
class Example1
{
public static void main(String args[])
{
try
{
System.out.println("Starting of try block");// throwing custom exception using throw
throw new MyException("This is My error Message");
}
catch(MyException exp)
{
System.out.println("Catch Block") ;
System.out.println(exp) ;
}
}}
```

### Problem Definition 2: Define custom exception to display product invalid error message.

```
class InvalidProductException extends Exception
{
public InvalidProductException(String s)
{
// Call constructor of parent Exception
super(s);
}
}
public class Example2
{
void productCheck(int weight) throws InvalidProductException{
if(weight<100){throw new InvalidProductException("Product Invalid");}
}
public static void main(String args[])
{
Example1 obj = new Example1();
try
{
obj.productCheck(60);
}
catch (InvalidProductException ex)
{System.out.println("Caught the exception"); System.out.println(ex.getMessage()); }
}}
```


## 12 Write a program to display sequence A1B2C3D4E5F6G7H8I9J10 using two child threads (Program on Multithreading)

```
class A extends Thread
{
public void run()
{
for (int i=1;i<=10;i++)
{
System.out.print(i);
try
{
Thread.sleep(500);
}
catch(InterruptedException e) {System.out.println("thread A interupted"+e);}
}}}
class B extends Thread
{
public void run()
{
for (char i=65;i<=74 ;++i )
{
System.out.print(i);
try
{
Thread.sleep(500);
}
catch(InterruptedException e) {System.out.println("thread binterrupted"+e);}
}}}
class MTDemo
{
public static void main (String args [])
{
A a=new A();
a.start();
B b=new B();
b.start();
try
{
a.join();
b.join();
}
catch (InterruptedException e)
{
System.out.println("main thread interrupted"+e);
}}}
```

## 13 Write a program to implement methods of Graphics class. 

```
import java.applet.Applet;
import java.awt.*;
/*
<applet code="GraphicsDemo.class" width="300" height="300">
</applet>
*/
public class GraphicsDemo extends Applet
{
public void paint(Graphics g)
{
g.setColor(Color.red);
g.drawString("Welcome",50, 50);
g.drawLine(20,30,20,300);
g.drawRect(70,100,30,30);
g.fillRect(170,100,30,30);
g.drawOval(70,200,30,30);
g.setColor(Color.pink);
g.fillOval(170,200,30,30);
g.drawArc(90,150,30,30,30,270);
g.fillArc(270,150,30,30,0,180);
}
}
```


## 14    Program to implement functions of Color and Font classes.

### 14.1  Write a program to implement methods of Color class. 

```
import java.applet.Applet;
import java.awt.*;
/*
<applet code="ColorDemo.class" width="300" height="300">
</applet>
*/
class ColorExample extends Frame
{
ColorExample()
{
Color frameColor = new Color(0,255,255);
setLayout(new FlowLayout());
setBackground(frameColor);
Button btnCancel = new Button("Cancel");
btnCancel.setBackground(Color.BLACK);
btnCancel.setForeground(Color.WHITE);
add(btnCancel);
}
}
public class ColorDemo
{
public static void main(String args[])
{
ColorExample frame = new ColorExample();
frame.setTitle("Color in Java Example");
frame.setSize(400,150);
frame.setVisible(true);
}
}
```

### 14.2 Write a program to implement methods of Font class.

```
import java.applet.Applet;
import java.awt.Font;
import java.awt.Graphics;
/*
<applet code="FontDemo.class" width="600" height="300">
</applet>
*/
public class FontDemo extends Applet
{
public void paint(Graphics g)
{
//creating a constructor of the font class and passing name, style, and size of the font
//we can change these three parameters accordingly
Font font1= new Font("Courier", Font.PLAIN, 20);
//setting font by invoking the setFont() method
g.setFont(font1);
g.drawString("Anil Satyadeo Londhe", 10, 40);
Font font2= new Font("Courier", Font.BOLD, 20);
g.setFont(font2);
g.drawString("Deepa Anil Londhe", 10, 70);
Font font3= new Font("Courier", Font.ITALIC, 20);
g.setFont(font3);
g.drawString("Aditya Anil Londhe", 10, 100);
}
}
```

## 15 Write a program to add two numbers entered via TextField AWT controls.(Program to create GUI application using AWT controls.)

```

import java.applet.*;
import java.awt.*;
import java.awt.event.*;
/*
<applet code="GUIApp.class" width=400 height=100 >
</applet>
*/

public class GUIApp extends Applet implements ActionListener
{
TextField firstNum, secondNum, resultNum;
public GUIApp()
{
setLayout(new GridLayout(3, 2, 10, 15));
setBackground(Color.cyan);
firstNum = new TextField(15);
secondNum = new TextField(15);
resultNum = new TextField(15);
secondNum.addActionListener(this);
add(new Label("Enter First Number")); add(firstNum);
add(new Label("Enter Second Number")); add(secondNum);
add(new Label("S U M")); add(resultNum);
}
public void actionPerformed(ActionEvent e)
{
String str1 = firstNum.getText();
double fn = Double.parseDouble(str1);
double sn = Double.parseDouble(secondNum.getText());
resultNum.setText("Sum is " + (fn+sn));
}
}

```



