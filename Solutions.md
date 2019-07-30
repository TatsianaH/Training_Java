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