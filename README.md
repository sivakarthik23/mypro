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
