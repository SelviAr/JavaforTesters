# JavaforTesters


##Table of Contents

- [Download Driver](#Driver-Download)
- [WebDriver](#setup)


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
	
	public int Divide(int a, int b){
		return a / b;
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
