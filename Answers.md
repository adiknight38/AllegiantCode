Aditya Patil	{#welcome}
---
3.The Challenge
---

>##3.1 Answers
>1.  I follow multiple websites such as stackoverflow,stackexchange to clear various queries I have and read through informative sites such as  javarevisited.com,IBM blogs and other user blogs from vogella and mkyoung to keep myself updated. I have also registered for courses on Coursera which had helped me work on my skill set.

>2. I use the following tools for developing software:
    >>2.1 Eclipse: Extensively for Java code as well as J2EE technologies
    >>2.2 MySQL/Oracle11g: Databases to test code underdevelopment
    >>2.3 JUnit 4.0 for testing individual modules and Eclemma to test code coverage
    >>2.4 I am familier with Tomcat WAS as well as Clearcase and ClearQuest tools for code management.
    >>2.5 There are other tools such as gcc compiler for C code and Visual Studio for C# that I have used.
    
>3. Coding excites me as I like to spend time on tackling multiple problems and if possible, figuring how to relate a particular solution to another problem. I especially enjoy object oriented programming as I find it easy to imagine various applications of the concepts relevant to OOD to develop a solution for an idea. I also enjoy working on low level C code as various factors need to be considered when space along with time restrictions are there. 

>4. I wish to become a master in Java as I want to learn the behind the scenes of various API calls that have been made available and possibly contribute in further development. 

>5. OOP is a concept that targets in handling large application level code so as to gain high coupling but low cohesion. Various concepts such as Abstraction,Inheritance, Polymorphism and Composition can be applied to achieve that purpose.

>6. TDD is a development plan so as to effectively test code at each level of the SDLC, all the way from creating test plans from documentation, to developing white box testing such as Unit tests, functional tests, integration tests as well as regression tests. This also includes performing black box testing via smoke and system testing.

>7. I use Junit to unit test and Eclemma for code coverage.I have also used PMD for statistical testing of code violations. Further I have used tools such as Apache Jmeter for Stress testing as well as Webscarab for penetration testing

>8. Strategy pattern is used for developing highly coupled code through composition.
To give an example: Lets consider a shooting game .
We have a abstract class called character which is composed of a reference of weapon interface. Many different concrete implementations of the character class can be created and also of the weapon interface and accordingly each character will have the privilge to choose the weapon to be used.

>9. Decorator pattern is used to give additional useful functionality for a concrete implementation.
Example: Java API calls such as buffered reader/writer provide synchronization mechanism for concrete implementations  of File reader/writer classes.

>10. For functional programming we essentially target evaluating mathematical functions and avoid the state of the data. example: Haskell,Lisp

----------

>##3.2 Code
>1. Java code for FizzBuzz
<pre>
public class FizzBuzz {
	// program that prints the numbers from 1 to 100.
	// But for multiples of three print "Fizz" instead of the number and for
	// multiples of five print "Buzz."
	// For numbers which are multiples of both three and five print "FizzBuzz."
	public static void main(String args[]) {
		//Loop from 1 to 100
		for (int currentNumber = 1; currentNumber <= 100; currentNumber++) {
			if (currentNumber % 3 == 0) 
			//Check if the number is divisible by 3
				System.out.print("Fizz");
			if (currentNumber % 5 == 0) 
			//Check if the number is divisible by 5
				System.out.print("Buzz");
			if (currentNumber % 3 != 0 && currentNumber % 5 != 0)
				//Simply print number if the number is not divisible by 3 or 5
					System.out.print(currentNumber); 
			System.out.println();
    		}
	    }
}

<code>

>2.  Java code for string operation

<pre>
public class StringToSpaces {
	
	public static String generateSpaces(String originalString)
	{
	    //store string as character array
		char[] characterSequence=originalString.toCharArray();
		
		//Use a stringbuilder as it is faster to concatenate as compared to the string          concatenation function
		StringBuilder stringBuider=new StringBuilder();
		
		//Loop through each character
		for(char current:characterSequence)
		{
			if(current==' ') //Chec if the character is a space
				stringBuider.append("[s]");
			else
			{   //copy as is
				stringBuider.append(current);
			}
			stringBuider.append(' ');
		}
		return new String(stringBuider);
	}
	public static void main(String args[]) {
		String originalString= new String("Hello World");
		String newString=generateSpaces(originalString);
		System.out.println("Original String: " + originalString);
		System.out.println("New String: " + newString);
	}
}
<code>
