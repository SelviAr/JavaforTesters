# JavaforTesters



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

