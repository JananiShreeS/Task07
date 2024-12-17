# Task07
1.division
package scanner;
import java.util.Scanner;
public class Division {

	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		try {
			System.out.println("Enter the Numerator");
			int numerator = sc.nextInt();
			
			System.out.println("Enter the denominator");
			int denominator =sc.nextInt();
			
			int result=numerator/denominator;
			System.out.println("The result is" +result);
		}
		
			catch (ArithmeticException e) {
			System.out.println("Error: Division by zero is not allowed.");
				
			}
			
		catch(Exception e) {
		System.out.println("Error: Invalid input. Please enter valid integers.");	
		}
		finally {
		sc.close();
		System.out.println("Program execution is Completed");
			
		}
				

	}

}

2.Arraybound
package scanner;
import java.util.Scanner;

public class Exceptions {
	
	public static void main(String[] args) {
	
Scanner sc = new Scanner(System.in);

try {
	System.out.println("ArrayIndexOutofBoundsException:");
	int[] numbers = {1,2,3,4,5};
	System.out.println("Enter the index to access(0-4)");
	int index=sc.nextInt();
	System.out.println("Element at index " + index + ": " + numbers[index]);
} catch (ArrayIndexOutOfBoundsException e) {
    System.out.println("Error: Array index is out of bounds!");
}
try {
    System.out.println("\nStringIndexOutOfBoundsException Example:");
    String text = "HelloWorld";
    System.out.print("Enter the index to access (0-9): ");
    int strIndex = sc.nextInt();
    System.out.println("Character at index " + strIndex + ": " + text.charAt(strIndex));
} catch (StringIndexOutOfBoundsException e) {
    System.out.println("Error: String index is out of bounds!");
}

System.out.println("\nProgram execution completed.");
sc.close();
}
	}

InvalidAge
package scanner;
import java.util.Scanner;

public class Invalidage {
	
	class InvalidAgeException extends Exception
	{
		public InvalidAgeException(String message)
		{
			super(message);
		}
		
	}

	class Main
	
	{
		public void checkAge(int age)
		throws InvalidAgeException {
			if(age<18) {
				throw new InvalidAgeException("Invalid Age:");	
			}
			else
			{
				System.out.println("Age " + age + " is valid. You are allowed to proceed.");
			}
			
		}
		public void main(String[] args) {
			Scanner scanner = new Scanner(System.in);

	        try {
	            
	            System.out.print("Enter your age: ");
	            int age = scanner.nextInt();

	            checkAge(age);
	        } catch (InvalidAgeException e) {
	           
	            System.out.println("Exception: " + e.getMessage());
	        } catch (Exception e) {
	          
	            System.out.println("An unexpected error occurred: " + e.getMessage());
	        } finally {
	            System.out.println("Program execution completed.");
	        }

	        scanner.close();
	}
	}

}

4.filenotbound

package scanner;
import java.util.Scanner;
import java.io.File;
import java.io.FileNotFoundException;

public class Filenotfound {

	public static void main(String[] args) {
	String filepath ="data.txt";
	try
	{
		File f = new File (filepath);
		Scanner filereader = new Scanner(f);
		
		System.out.println("Reading file contents:");
		while (filereader.hasNextLine()) {
			String line = filereader.nextLine();
			System.out.println(line);
	
		}
		filereader.close();
	}
	
		
		catch(FileNotFoundException e) {
			System.out.println("Error:The File\"" +filepath+ "\" was not found");
			System.out.println("Please check the file name or path and try again");
			
		}
			
		}
	}

 package scanner;

import java.util.ArrayList;
import java.util.List;

public class Listtoarray {

public static void main(String[] args) {
	List<String> list = new ArrayList<>();
	list.add("Java");
	list.add("Program");
	list.add("Guvi");
	list.add("JAT-WD-E-B6");
	
	System.out.println("List" +list);
	
	String[] array=list.toArray(new String[0]);
	
	System.out.println("Converted Array:");
	for(String element : array) {
        System.out.println(element);
    }
}
}


package scanner;
import java.util.ArrayList;

public class Removeelements {

public static void main(String[] args) {
	ArrayList<String> stringlist = new ArrayList<>();
	stringlist.add("Pineapple");
	stringlist.add("Apple");
	stringlist.add("guava");
	stringlist.add("Banana");
	
	System.out.println("String List" +stringlist);
	
	stringlist.clear();
	
	System.out.println("After removed string" +stringlist);
	

	}

}

package scanner;
import java.util.Map;
import java.util.Map.Entry;
import java.util.TreeMap;
import java.util.List;
import java.util.Collections;
import java.util.Iterator;
import java.util.ArrayList;
public class Treemap {

	private static Entry<Integer, String> entry;

	public static void main(String[] args) {
		
TreeMap<Integer,String> employeemap =new TreeMap<>();
employeemap.put(001,"Anish");
employeemap.put(002,"Hema");
employeemap.put(003,"Dhivya");
employeemap.put(004,"Arun");
employeemap.put(005,"Raju");
employeemap.put(006,"Feba");

System.out.println("Employee Map:");

for (Iterator<Entry<Integer, String>> iterator = 
employeemap.entrySet().iterator(); iterator.hasNext();)
{
Map.Entry<Integer,String> entry = iterator.next();

for(Map.Entry<Integer,String> entry1 : employeemap.entrySet());
{
	System.out.println("ID:" +entry.getKey()+",Name:" +entry.getValue());
	
}
List<String> employeeNames = new ArrayList<>(employeemap.values());
Collections.sort(employeeNames);

System.out.println("\nEmployee Names in Alphabetical Order:");
for (String name : employeeNames) 
{
    System.out.println(name);
}


	}

	}
}
