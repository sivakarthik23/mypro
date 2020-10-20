# mypro
demo
public class filedownload {

	public  static void main(String[] args) {
		// TODO Auto-generated method stub

	
		
	 System.setProperty("webdriver.chrome.driver" ,"C:\\Users\\SSC\\Downloads\\chromedriver_win32\\chromedriver.exe" );
     WebDriver driver = new ChromeDriver();					
 String URL = "http://the-internet.herokuapp.com/download";
  driver.get(URL);
  driver.manage().window().maximize();
  driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS);
     WebElement link= driver.findElement(By.linkText("hello_world.txt"));	
     
     boolean dsp =link.isEnabled();
     System.out.println("is enabled" +dsp);
    
     System.out.println("file downloaded" +link);
     driver.close(); 
}
	
}

public class Checkbox {

	public  static void main(String[] args) {
		// TODO Auto-generated method stub

	
		
	 System.setProperty("webdriver.chrome.driver" ,"C:\\Users\\SSC\\Downloads\\chromedriver_win32\\chromedriver.exe" );
     WebDriver driver = new ChromeDriver();					
 String URL = "https://the-internet.herokuapp.com/checkboxes";
  driver.get(URL);
  driver.manage().window().maximize();
  driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS);
     WebElement checkbox1 = driver.findElement(By.xpath("(//input[@type ='checkbox'])[1]"));	
     Boolean dis =checkbox1.isDisplayed();
     System.out.println("checkbox displayed" +dis);
    boolean val= checkbox1.isSelected();
System.out.println("selected " +val);
     WebElement  checkbox2 = driver.findElement(By.xpath("(//input[@type ='checkbox'])[2]"));	
     Boolean disp =checkbox2.isDisplayed();
     System.out.println("checkbox displayed" +disp);
     boolean val1 = checkbox2.isSelected();
     System.out.println("selected " +val1);
     driver.close(); 
}
	
}
