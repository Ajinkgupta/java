# Experiment No: 1
### Aim: Program on branching, looping, labeled break and labeled continue
### Theory:
There may be a situation when you need to execute a block of code several number of times. In general, statements are executed sequentially: The first statement in a function is executed first, followed by the second, and so on. Programming languages provide various control   structures   that   allow   for   more   complicated   execution   paths.
A loop statement allows us to execute a statement or group of statements multiple times and following is the general form of a loop statement in most of the programming languages −
**While loop** Repeats a statement or group of statements while a given condition is true. It tests the condition before executing the loop body.
For loop Execute a sequence of statements multiple times and abbreviates the code that manages the loop variable.
**do...while loop** Like a while statement, except that it tests the condition at the end of the loop body.
Loop control statements change execution from its normal sequence. When execution leaves a scope, all automatic objects that were created in that scope are destroyed.Java supports the following control statements.
The break statement in Java programming language has the following two usages
−The continue keyword can be used in any of the loop control structures. It causes the loop to immediately jump to the next iteration of the loop. 

### code

```
public class PrimeCheck
{    
 public static void main(String args[])
{    
  int i,m=0,flag=0;      
  int n=3;//it is the number to be checked    
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
 } //end of inner if     
 } //end of for       

if(flag==0)  { System.out.println(n+" is prime number"); }  
} //end of outer else  
} //end of main function  
} //end of class

```
### Output

```3 is prime number ```

