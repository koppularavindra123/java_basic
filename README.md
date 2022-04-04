# java_basic

package dev;
import java.io.*;
public class Digit {
	public static void main(String args[])throws Exception
	{
		InputStreamReader isr=new InputStreamReader(System.in);
		BufferedReader br=new BufferedReader(isr);
		int a;
		a=Integer.parseInt(br.readLine());
		if (a==0)
			System.out.println("zero");
		else if (a==1)
			System.out.println("one");
		else if (a==2)
			System.out.println("two");
		else if (a==3)
			System.out.println("three");
		else if (a==4)
			System.out.println("four");
		else if (a==5)
			System.out.println("five");
		else if (a==6)
			System.out.println("six");
		else if(a==7)
			System.out.println("seven");
		else if (a==8)
			System.out.println("Eight");
		else if (a==9)
			System.out.println("Nine");
		else
			System.out.println("Please Enter the single Digit Number ");
	}

}

// program to check given  num is amstrong or not
package koppula;
import java.io.*;
public class Amstrong {
	public static void main(String args[])throws Exception
	{
		InputStreamReader isr=new InputStreamReader(System.in);
		BufferedReader br=new BufferedReader(isr);
		int n,k,c=0,arm=0,a;
		n=Integer.parseInt(br.readLine());
		k=n;
		a=n;
		c=(int)Math.log10(n)+1;
		while(n>0)
		{
			arm+=Math.pow((n%10),c);
			n=n/10;
		}
		if(a==arm) {
			System.out.println("The given num is an armstrong number");
		}
		else
		{
			System.out.println("The given num is not an armstrong number");
		}
	}

}

// switch case program

package koppula;
import java.io.*;
public class Color {
	public static void main(String[] args)throws Exception
		{
			InputStreamReader isr=new InputStreamReader(System.in);
			BufferedReader br=new BufferedReader(isr);
			char ch;
			ch=(char)br.read();
			switch(ch)
			{
			case 'Y':
				System.out.println("yellow");
				break;
			case 'R':
				System.out.println("red");
				break;
			case 'G':
				System.out.println("green");
				break;
			case 'B':
				System.out.println("blue");
				break;
			case 'V':
				System.out.println("violet");
				break;
			case 'O':
				System.out.println("orange");
				break;
			case 'I':
				System.out.println("Indigo");
				break;
				default:
				System.out.println("color didn't match");
			}
			
			}
	}


// program to check the given num is fibonacci or not
package koppula;
import java.io.*;
public class Fibonacci {
	public static void main(String args[])throws Exception
	{
		InputStreamReader isr=new InputStreamReader(System.in);
		BufferedReader br=new BufferedReader(isr);
		int a=0,b=1,n,c,sum=0;
		n=Integer.parseInt(br.readLine());
		for(int i=2;i<n;i++)
		{
		c=a+b;
		a=b;
		b=c;
		if(b%2==0) {
			sum+=b;
		}
		}
		System.out.print(sum);
	}
}

// methods in java
package koppula;
import java.io.*;
public class Methods {
	public  void display() //static method
	{
		System.out.println("hi, i am koppula");
		
	}
	public void show()// non static method
	{
		System.out.println("hello, this is VIjju");
	}
	public static void main(String args[])// main method
	{
		Methods obj=new Methods();
		obj.display();
		obj.show();
		}

}

// no of digits in a given number:
package koppula;
import java.io.*;
public class No_of_digits {
	public static void main(String args[])throws Exception
	{
		InputStreamReader isr=new InputStreamReader(System.in);
		BufferedReader br=new BufferedReader(isr);
		int n,a,temp,r,sum=0;
		n=Integer.parseInt(br.readLine());//  input number :145= 
		temp=n;
		a=(int)Math.log10(n)+1; // no of digits =3
		while(n>0) {
			r=n%10;// last digit=4
			sum+=Math.pow(r, a);//125+16+11=145 
			n=n/10;
			a--;
	}
		if(sum==temp) {
			System.out.println(temp+" is a disirium number");
		}
		else {
		System.out.println(temp+" is not a disirium number");
		}
		
		
	}

}

// program to check the given num is palindrome or not
package koppula;
import java.io.*;
public class Palindrome {
	public static void main(String args[])throws Exception
	{
		InputStreamReader isr=new InputStreamReader(System.in);
		BufferedReader br=new BufferedReader(isr);
		int n;
		System.out.println("Enter a number:");
		int r,s=0;
		n=Integer.parseInt(br.readLine());
		int k=n;
		while(k>0)
		{
			r=k%10;
			s=s*10+r;
			k=k/10;
		}
		if(s==n) {
			System.out.println(s+" is a palindrome number.");
		}
		else {
		System.out.println(s+ "not a palindrome number:");
		}
	}
}

// program to print all the primes within the range
package koppula;
import java.io.*;
public class Prime_Range {
	public static void main(String args[])throws Exception
	{
		InputStreamReader isr=new InputStreamReader(System.in);
		BufferedReader br=new BufferedReader(isr);
		int n=2,count;
		while (n<=100)
		{
			count=0;
			for(int i=1;i<=n;i++)
			{
				if(n%i==0)
					count++;
			}
			if (count==2)
				System.out.print(n+" ");
			n++;	
		}
	}

}

//program to check given num is prime or not 
package koppula;
import java.io.*;
public class Prime{
	public static void main(String args[])throws Exception
	{
		InputStreamReader isr=new InputStreamReader(System.in);
		BufferedReader br=new BufferedReader(isr);
		System.out.println("Enter a number:");
		int n,flag=0;
		n=Integer.parseInt(br.readLine());
		if (n==1 || n==0)
			System.out.println(n);
		else
			for(int i=2;i<n;i++)
			{
				if (n%i==0)
					flag=1;
			}
		if (flag==1)
			System.out.println(n+" is not a prime number:");
		else
			System.out.println(n+ " is a prime number:");
}
}

// sum of primes(geeeksforgeeks)
package koppula;
import java.io.*;
public class PrimeSum {
	public static void main(String args[])throws Exception
	{
		InputStreamReader isr=new InputStreamReader(System.in);
		BufferedReader br=new BufferedReader(isr);
		System.out.println("Enter a Number:");
		int n,s=0,r;
		n=Integer.parseInt(br.readLine());
		while(n>0)
		{
			r=n%10;
			if (r==2 || r==3 || r==5 || r==7)
				s+=r;
			n=n/10;
		}
			System.out.println(s);
			
		}
			
	}
  
  // given char is vowel or not using switch case:
  package koppula;
import java.io.*;
public class Vowel {
	public static void main(String args[])throws Exception
	{
		InputStreamReader isr=new InputStreamReader(System.in);
		BufferedReader br=new BufferedReader(isr);
		char ch;
		ch=(char)br.read();
		switch(ch)
		{
		case 'A':
		case 'E':
		case 'I':
		case 'O':
		case 'U':
			System.out.println("vowel");
			break;
			default:
			System.out.println("consonant");
		}
		
		}
}






