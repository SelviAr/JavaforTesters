# JavaforTesters

http://www.seleniumeasy.com/java-tutorials

##Table of Contents

- [Class](#Class)
- [Data Type](#data-type)


```java
/*
 * package, import, class and method
 */

package com.selvenium.web;

//Import
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.firefox.FirefoxDriver;

import org.testng.annotations.Test;

//create a public class
public class ForTesters {
	
	//Create a public method TestGoogle, it returns nothing 
	@Test //Annotation
	public void TestGoogle(){
		WebDriver driver = new FirefoxDriver();           
		driver.get("https://www.google.com");
		driver.findElement(By.name("q")).sendKeys("Download selenium chrome driver");
		driver.findElement(By.id("butid")).click();
		System.out.println(driver.getTitle());
		driver.quit();
	}
	
	//Define a private method that returns string data
	private String GetGreetings(){
		return "Welcome";
	}
	
}
```

## Class

### Calculator Class

```java
//Class Calculator provides addition, subtraction, division and multiplication functionality
public class Calculator {

	public int Add(int a, int b){
		int c = a + b;
		return c;
	}
	
	public int Subtract(int a, int b){
		return a - b;
	}
	
	public int Multiply(int a, int b){
		return a * b;
	}
	
	public int Divide(int a, int b) throws ZeroDivisionException{
	
	 try {
		return a / b;
	     } catch (ZeroDivisionException e) {	
	     	System.out.println(e.getMessage());
	     }
	}
  }

}
```


### Calculator Class

```java
//Class AdvancedCalculator extends Calculator
//Advanced Calculator provides SqureRoot, PI value and also addition, subtraction, division and multiplication functionality
public class AdvancedCalculator extends Calculator  {

	public int SqureRoot(int a){
		int c = a * a;
		return c;
	}
	
	public double GetPI(){
		return 3.14;
	}
}

```




### Test Advanced Calculator Class

```java

package com.selvenium.web;

import org.testng.Assert;
import org.testng.annotations.BeforeTest;
import org.testng.annotations.Test;

public class TestCalculator {
	
	AdvancedCalculator advCalc;
	
	@BeforeTest
	public void setup(){
		advCalc = new AdvancedCalculator();
	}
	
	@Test
	public void TestAdd(){
		Assert.assertEquals(advCalc.Add(10, 5), 15);
	}
	
	@Test
	public void TestPIValue(){
		Assert.assertEquals(advCalc.GetPI(), 3.50);
	}
	
	@Test
	public void TestSqRoot(){
		Assert.assertEquals(advCalc.SqureRoot(10), 100);
	}
}


```


## Data Type

```java


//Integer
int age = 1;
byte maxAge = 100;
short s = 10000;
long creditCardNumber = 1234_5678_9012_3456L;

//Floating-Point Literals
double d1 = 123.4;
double d2 = 1.234e2;	// same value as d1, but in scientific notation
float f1  = 123.4f;

boolean isApproved = true;
char capitalS = 'S';

String myName = "Selvi";

//Data Type
String $aString="bob";
float £owed=10F;
int aMount=4;
long Amount=5;
String A0123456789bCd$f="ugh";
boolean truthy = true;
boolean falsey = false;
byte range: -128 to 127
short range: -32768 to 32767
int range: -2147483648 to 2147483647
long range: -9223372036854775808 to 9223372036854775807

float singlePrecision32bit;
double doublePrecision64bit;


```


## Field Access

```java
public static final String CONSTANT = "a constant string";
public static String aClassField = "a class field";
protected static String proField = "a class field";
public String pubField = "a public field";
private String privField = "a private field";
private String name;
```
	
	
	
## if conditions

```java
//if conditions
	int mynumber = 999;
	
	if (mynumber == 999) {
	    System.out.println("this is lucky nymber");
	}

	//if then else conditions
	if (a >= b) {
		System.out.println("a is greater than b");
	} else {
		System.out.println("b is greater than a");
	}


	//if then else if conditions
	if (a >= b) {
		System.out.println("a is greater than b");
	} else if (b >= c) {
		System.out.println("b is greater than c");
	}
		
```



## for loop

```java
// Collection-Based For Loop
String[] workdays = {"Monday", "Tuesday", "Wednesday", "Thursday", "Friday"};

//foreach loop
for(String workday : workdays){
System.out.println(workday); 
}

//for loop with index 		
for(int i=0; i<5; i++){
System.out.println(workdays[i]); 
}
		
```

## while loop

```java
int i = 0;
 
while (i < 3) {
	System.out.println(i);
	i++;
}

```

## do while loop

```java
int i = 0;
    do {
      System.out.println(i);
      i++;
    } while (i < 3);
```

## Methods

```java

public void getAge(){

}


public void getAge(int age){

}


public void getAge(int age, int status){

}


public int getAge(int age, int status){

}


```

## Array

```java

```

## Switch

```java

```

## Collection

```java

```
