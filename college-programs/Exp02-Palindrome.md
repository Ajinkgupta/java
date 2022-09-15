# Experiment 2
### Aim: To demonstrate various ways of accepting data through keyboard.
**Theory**: Input and Output streams


Data flows from one place to another place. This is said to be a stream. Java consists of two types of streams namely input and output streams. If you want to receive data then use input stream, if you want to display or write data then you can use output stream. In java, classes are used to represent these streams. These classes are stored in a package called java.io respectively.


**System .in**: An object belonging to an input-stream is represented by this command. It indirectly means a standard keyboard device.


**System.out**: If you want to represent an object belonging to the print-stream class, then use this command which indirectly means a standard output device.


**System.err**: Similar to the above command it also represents an object belonging to the print-stream class. But the difference is that, the above command displays a simple message, this one simply displays an error message.
The readLine() method of DataInputStream reads a line at a time and returns as a string, irrespective of what the line contains. Depending on the input value, the string is to be parsed into an int or double etc. " in" is an object of " InputStream" class defined in System class It is declared as static and final object. The in object is connected implicitly to the " standard input stream" of the underlying OS.

```
DataInputStream dis = new DataInputStream(System.in);
System.out.println("Enter Integer Number ");
n= Integer.parseInt(dis.readLine());
```

**System. in ** is a byte stream which is automatically connected to the keyboard reading mechanism of operating system. It is a low-level byte stream.
```Scanner class: Reading input through keyboard```

The keyboard is represented by the standard input stream (System.in). The keyboard is linked with scanner for easier way of writing java program. An object of type scanner needs to be created to make the use of the method in it for reading various types keyboard input.
```
Scanner scan = new Scanner(System.in);
System.out.println("Enter Integer Number ");
n=scan.nextInt();
```
##### Program to check whether the number is palindrome or not. Accept input from keyboard.
### CODE
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
   r=n%10;  //getting remainder  
   sum=(sum*10)+r;    
   n=n/10;   //getting quotient   
 }  // end of while
  
  if (temp==sum)    System.out.println("palindrome number ");    
  else   System.out.println("not palindrome");    

}  // end of main function
}  // end of class

```

### Output

```
D:\java>java PalindromeCheck 454
palindrome number
D:\java>java PalindromeCheck 4545
not palindrome


```

