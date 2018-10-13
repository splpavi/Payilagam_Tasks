# Payilagam_Tasks
package oxygen.com;

import java.util.Scanner;

public class Avg {

	public static void main(String[] args) {
    try {
	String a="";
	int sum=0,avg;
	Scanner s=new Scanner(System.in);
    System.out.println("Enter the number of inputs");
    String d=s.next();
    int n=Integer.parseInt(d);
	int b[]=new int[10];
    if(n<=0)
	{
    	throw new MyException();
	}
      System.out.println("Enter the inputs");
    for(int i=0;i<n;i++)
    {
    	a=s.next();
    b[i]=Integer.parseInt(a);
    sum=b[i]+sum;
    }
    avg=sum/n;
    System.out.println("The sum is:"+sum);
    System.out.println("The average is:"+avg);
    }
    catch(MyException e)
    {
    	System.out.println(e.getMessage());
    }
    catch(NumberFormatException e)
    {
    	System.out.println(e);
    }
    catch(ArrayIndexOutOfBoundsException e)
    {System.out.println(e);}
    }
    
    }
}
class MyException extends Exception
{
	MyException()
	{
	super("Number should be greater than zero");
	}
	
}



//OUTPUT:Enter the number of inputs
//2
//Enter the inputs
//1
//2
//The sum is:3
//The average is:1
//
