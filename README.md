*Even or Odd*
https://www.codewars.com/kata/53da3dbb4a5168369a0000fe/train/java
```java
public class EvenOrOdd {
    public static String even_or_odd(int number) {
       if(number % 2 == 0) {
           return "Even";
       } else {
           return "Odd";
       }
    }
}
```
*Opposite number*
https://www.codewars.com/kata/56dec885c54a926dcd001095/train/java
```java
public class Kata{
    public static int opposite(int number){
        return number * (- 1);
    }
}
```
*2 variant*
```java
public class Kata{
    public static int opposite(int number){
        if(number > 0){
            return number * (-1);
        } else {
            return 0 - number;
        }   
    }
}
```
*3 variant*
```java
public class Kata
    {
        public static int opposite(int number)
        {
           if(number > 0){
           return (-number);
           } else {
           return (number * (-1));
           }
        }
    }
```
*final solution*
```java
public class Kata{
    public static int opposite(int number){
        if(number > 0){
            return number * (-1);
        } else {
            return 0 - number;
        }   
    }
}
```

*Find the smallest integer in the array*
https://www.codewars.com/kata/55a2d7ebe362935a210000b2/train/java
```java
public class SmallestIntegerFinder {
    public static int findSmallestInt(int[] args) {
        int min = args[0];
        for(int i = 0; i < args.length; i++){
            if(min > args[i]){
              min = args[i];
            } 
        }
      return min;
    }
}
```


*Find the first non-consecutive number*
https://www.codewars.com/kata/58f8a3a27a5c28d92e000144/train/java
```java
class FirstNonConsecutive {
    static Integer find(final int[] arr) {
      for(int i = 0; i < arr.length - 1; i++){
        if(arr[i] - arr[i + 1] != -1){
          return arr[i + 1];
        }
      }
        return null;
    }
}
```
*Find the position!*
https://www.codewars.com/kata/5808e2006b65bff35500008f/train/java
```java
public class Kata{
  public static String position(char alphabet){
    String line = "abcdefghijklmnopqrstuvwxyz";
    return "Position of alphabet: " + (line.indexOf(alphabet) + 1);
  }
}
```


*Playing with cubes I*
https://www.codewars.com/kata/playing-with-cubes-i/train/java
```java
public class Cube{
  int Side;
  int getSide(){
    return this.Side;
  }
  void setSide(int Side){
    this.Side = Side;
  }
}
```

*Lombok Encapsulation*
https://www.codewars.com/kata/lombok-encapsulation/train/java
```java
public class EncapsulationDemo {
  private int number;
  private String stringValue;
  private Object anObject;

  public void setNumber(int number) {
    this.number = number;
  }
  public int getNumber() {
    return number;
  }

  public void setStringValue(String stringValue) {
    this.stringValue = stringValue;
  }
  public String getStringValue() {
    return stringValue;
  }

  public void setAnObject(Object anObject) {
    this.anObject = anObject;
  }
  public Object getAnObject() {
    return anObject;
  }

  public EncapsulationDemo() {
  };

  public EncapsulationDemo(int number, String stringValue, Object anObject) {
    this.number = number;
    this.stringValue = stringValue;
    this.anObject = anObject;
  };
}
```


*Building blocks*
https://www.codewars.com/kata/building-blocks/train/java
```java
public class Block{
  private int width;
  private int length;
  private int height;
  private int volume;
  private int surfaceArea;
  
  // Constructor
  public Block(int[] params) {
    this.width = params[0];
    this.length = params[1];
    this.height = params[2];
    
    volume = width * length * height;
    surfaceArea = 2 * (width * length + width * height + length * height);
  }
  
  public int getWidth() {
    return width;
  }
  
  public int getLength() {
    return length;
  }
  
  public int getHeight() {
    return height;
  }
  
  public int getVolume() {
    return volume;
  }
  
  public int getSurfaceArea() {
    return surfaceArea;
  }
}
```
*Square(n) Sum*
https://www.codewars.com/kata/515e271a311df0350d00000f/train/java
```java
public class Kata
 {
  public static int squareSum(int[] n)
  { 
   int sum = 0;
   for(int i = 0; i < n.length; i++){
     sum += n[i] * n[i];
     }
     return sum;
  }
 }
```
*Two fighters, one winner.*
https://www.codewars.com/kata/two-fighters-one-winner/train/java
```java
public class Kata {
    public static String declareWinner(Fighter fighter1, Fighter fighter2, String firstAttacker) {
        int i;
        if(firstAttacker == fighter1.name) {
            i = 1;
            for ( i = 1; (fighter1.health > 0) && (fighter2.health > 0); i++) {
                if (i % 2 == 0) {
                    fighter1.health -= fighter2.damagePerAttack;
                } else  {
                    fighter2.health -= fighter1.damagePerAttack;
                }
            }
        }
        if(firstAttacker == fighter2.name) {
            i = 0;
            for ( i = 0; (fighter1.health > 0) && (fighter2.health > 0); i++) {
                if (i % 2 == 0) {
                    fighter1.health -= fighter2.damagePerAttack;
                } else  {
                    fighter2.health -= fighter1.damagePerAttack;
                }
            }
        }

        if (fighter1.health > 0) {
            return fighter1.name;
        } else {
            return fighter2.name;
        }
    }
}
```
*2 version*
```java
public class Kata {
  public static String declareWinner(Fighter fighter1, Fighter fighter2, String firstAttacker) {
    Fighter a = fighter1; 
    Fighter b = fighter2;
    if (firstAttacker.equals(fighter2.name)) {
      a = fighter2; b = fighter1;
    }    
    while (true) {      
      if ((b.health -= a.damagePerAttack) <= 0) return a.name;  // a wins
      if ((a.health -= b.damagePerAttack) <= 0) return b.name;  // b wins
    }
  }
}
```
*3 case*
```java
public class Kata {
  public static String declareWinner(Fighter fighter1, Fighter fighter2, String firstAttacker) {
    while(true){
            fighter1.health -= fighter2.damagePerAttack;
            fighter2.health -= fighter1.damagePerAttack;
            if(fighter1.health <= 0 && fighter2.health <= 0) return firstAttacker;
            if(fighter1.health <= 0) return fighter2.name;
            if(fighter2.health <= 0) return fighter1.name;
  }
  }
}
```
*4 case*
```java
public class Kata {
  public static String declareWinner(Fighter fighter1, Fighter fighter2, String firstAttacker) {
   int count1 = (int)Math.ceil((double)fighter1.health/fighter2.damagePerAttack);
   int count2 = (int)Math.ceil((double)fighter2.health/fighter1.damagePerAttack);
   
   if(count1 < count2) return fighter2.name;
   if(count1 > count2) return fighter1.name;
   
   return firstAttacker;
   
  }
}
```
*Is it even?*
https://www.codewars.com/kata/555a67db74814aa4ee0001b5/train/java
```java
public class Number {

  public boolean isEven(double n) {
    if(n % 2 == 0){
    return true;
    } else {
    return false;
    }
  }
}
```
*N-th Power*
https://www.codewars.com/kata/57d814e4950d8489720008db/train/java
```java
public class Kata {
	public static int nthPower(int[] array, int n) {
		for (int i = 0; i < array.length; i++) {
			if (i == n) {
				return (int) Math.pow(array[i], n);
			}
		}
		return -1;
	}
}
```
*Tip Calculator*
https://www.codewars.com/kata/56598d8076ee7a0759000087/train/java
```java
public class TipCalculator {

  public static Integer calculateTip(double amount, String rating) {
		    rating = rating.toLowerCase();
		    switch(rating){
		    
        case "terrible":
		    return 0;
		    
        case "poor":
		    return (int) Math.ceil (amount * 0.05);
		   
		    case "good":
		    return (int) Math.ceil(amount * 0.1);
		 
		    case "great":
		    return(int) Math.ceil(amount * 0.15);
	
		    case "excellent":
		    return (int) Math.ceil(amount * 0.2);
	
		    default:
		    return null;
		    }
		}
}
```
*Regexp Basics - is it a digit?*
https://www.codewars.com/kata/567bf4f7ee34510f69000032/train/java
```java
public class StringUtils {
  
  public static boolean isDigit(String s) {
    return s.matches("^[0-9]$");
  }
}
```
*Surface Area and Volume of a Box*
https://www.codewars.com/kata/565f5825379664a26b00007c/train/java
```java
public class Kata {
    
	public static int[] getSize(int w,int h,int d) {
		int area = 2 * (w * h + h * d + w * d);
		int volume =  w * h * d;
		int [] arr = {area, volume}; 
	        return arr;
	}
}
```
*Fibonacci*
https://www.codewars.com/kata/57a1d5ef7cb1f3db590002af/train/java
```java
public class Fibonacci {
	public static long fib (int n){
   long a = 0, b = 1, c;
		if (n == 0) return a;
		if (n == 1) return b;
		for (int i = 2; i <= n; i++) {
			c = a + b;
			a = b;
			b = c;
		}
		return b;
	}
}
```
*Inheritance*
```java

public class Animal {

	private String type;
	
	//constructor
	public Animal(String aType) {
		type = aType;
	}
	//default constructor
	public Animal() {
		type = "";
	}
	//operations
	public void eat() {
		System.out.println("Eating...");
	}
//getter
	public String getType() {
		return type;
	}
	// we don't need to have setter here, because we already have the constructor
	//public void setType(String type) {
	//	this.type = type;
	//}
	
	
}

public class Dog extends Animal {

	private String name;
	private String breed;
	//constructor
	public Dog (String aType, String aName, String aBreed) {
		super (aType);
		name = aName;
		breed = aBreed;
	}
	//operations
	public void bark() {
		System.out.println("Barking");
	}
	public String getName() {
		return name;
	}
	public String getBreed() {
		return breed;
	}
	public void eat() {
		System.out.println("Eating bones");
	}
	
}


public class TestInheritance {

	public static void main(String[] args) {

Dog dog = new Dog("Small dog", "Tuzik", "Chihuahua");
dog.bark();
dog.eat();	
System.out.println("Dog's type: " + dog.getType());
System.out.println("Dog's name: " + dog.getName());

Animal animal = new Animal("A scary animal");

Animal a = new Dog("Very big dog", "Rex", "Labrador");
System.out.println("Dog's type: " + a.getType());
a.eat();
	}

}
```
*Inheritance, package, array*
```java
//Person class
package person;

public class Person {
	private String name;
	private int age;
	private char sex;

	public Person(String name, int age, char sex) {
		this.name = name;
		this.age = age;
		this.sex = sex;
	}

	protected String getBaseName() {
		return this.name;
	}

	public String getName() {
		return (sex == 'W' ? "Ms. " : "Mr. ") + name;
	}

	public int getAge() {
		return age;
	}

	public int getSex() {
		return sex;
	}
}
//Employee class
package person;

public class Employee extends Person {
	
	private int salary;

	public Employee(String name, int age, char sex, int salary) {
		super(name, age, sex);
		this.salary = salary;
	}

	public boolean isSameName(Employee employee) {
		return getBaseName().equals(employee.getBaseName());

	}

	public int getSalary() {
		return salary;
	}
}
//Salary class
package person;

public class Salary {

	public int getSum(Employee... employeeArray) {
		int res = 0;
		for (int i = 0; i < employeeArray.length; i++) {
			res += employeeArray[i].getSalary();
		}
		return res;
	}
}
//TestPerson
package person;

public class TestPersonSerg {

	public static void main(String... args) {

		Employee employee1 = new Employee("Mike", 30, 'M', 300);
		Employee employee2 = new Employee("Mila", 31, 'M', 500);
		
		Salary salary = new Salary();
		int sum = salary.getSum(employee1, employee2);
		
		System.out.println(sum);

	}
}
```
**
```java
//DateUtils Class

public class DateUtils {

	public static class Month {
		private String name;
		private int days;
		private int workDays;

		public Month(String name, int days, int workDays) {
			this.name = name;
			this.days = days;
			this.workDays = workDays;
		}

		public String getName() {
			return name;
		}

		public int getDays() {
			return days;
		}

		public int getWorkDays() {
			return workDays;
		}
	}

	private static final Month[] months = { new Month("January", 31, 24), new Month("February", 28, 19) };

	public static Month[] getMonths() {
		return months;

	}
	public static int getSalary(Employee employee, Month[] monthArray) {
		int workDays = 0;
		for(int i = 0; i < monthArray.length; i++) {
			workDays += monthArray[i].getWorkDays();
		}
		return employee.getSalary() * workDays;
	}
}

//Employee class


public class Employee {

	private String  name;
	private int age;
	private char sex;
	private int salary;
	
	public Employee(String name, int age, char sex, int salary) {
		this.name = name;
		this.age = age;
		this.sex = sex;
		this.salary = salary;
	}
	public String getName() {
		return name;
	}
	public void setName(String name) {
		this.name = name;
	}
	public int getAge() {
		return age;
	}
	public void setAge(int age) {
		this.age = age;
	}
	public char getSex() {
		return sex;
	}
	public void setSex(char sex) {
		this.sex = sex;
	}
	public int getSalary() {
		return salary;
	}
	public void setSalary(int salary) {
		this.salary = salary;
	}
	
	/*public int getSalary(DateUtils.Month[] monthArray) {
		int workDays = 0;
		for(int i = 0; i < monthArray.length; i++) {
			workDays += monthArray[i].getWorkDays();
		}
		return this.getSalary() * workDays;
	}*/
	
	
}
//Manager Class

public class Manager extends Employee {

	private int countOfEmployee;

	public Manager(String name, int age, char sex, int salary, int countOfEmployee) {
		super(name, age, sex, salary);
		this.countOfEmployee = countOfEmployee;
	}

	public int getCountOfEmployee() {
		return countOfEmployee;
	}

	public void setCountOfEmployee(int countOfEmployee) {
		this.countOfEmployee = countOfEmployee;
	}

}
//TestHWSerg3

public class TestHWSerg3 {

	public static void main(String[] args) {

		Employee employee = new Employee("Joe", 30, 'M', 100);

		System.out.println(DateUtils.getSalary(employee, DateUtils.getMonths()));
	}

}
```
*Arrays*
```java

public class WorkingWithArrays {

	public static void main(String[] args) {
//array declaration		
		int[] myArray;
		int myArray2[];// 2nd case of C++ representation
		myArray = new int[66];// create length of array
		myArray[0] = 24;

		String myString2[];
		String[] myString = new String[2];
		myString[0] = new String("Tony");// можно задавать 2 способами String
		myString[1] = "Vlad";//

		for (int i = 0; i < myString.length; i++) {
			System.out.println(myString[i]);// если хотим распечатать элементы массива
		}

// array initialization
		String[] family = { "Mama", "Papa" };
		
// for each
		for(String string: family) {
			System.out.println(string);
		}
		

	}

}
```
```java
import java.util.Arrays;

public class ArrayComparison {

	public static void main(String[] args) {
String[] books1 = {"War and Peace", "Farewell to Arms", "Hamlet"};
String[] books2 = {"War and Peace", "Farewell to Arms", "Hamlet"};

if(books1 == books2)
	System.out.println("==: Books are not equal");
	
	if(Arrays.equals(books1, books2))
		System.out.println("equals: Books are equal");
	}

}
```
**