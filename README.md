# selenium2
package newpack;
import org.openqa.selenium.*;
import org.openqa.selenium.firefox.*;
import org.openqa.selenium.support.ui.Select;
import org.xml.*;

public class firstclass {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
WebDriver driver=new FirefoxDriver();
driver.manage().window().maximize();
driver.get("https://book.spicejet.com/register.aspx");
WebElement DAY=driver.findElement(By.id("CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_DropDownListDOBDay"));
WebElement MONTH=driver.findElement(By.id("CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_DropDownListDOBMonth"));
WebElement YEAR=driver.findElement(By.id("CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_DropDownListDOBYear"));
Select sel=new Select(DAY);
sel.selectByValue("10");
Select sel1=new Select(MONTH);
sel1.selectByVisibleText("june");
Select sel2=new Select(YEAR);
sel2.selectByValue("20");
driver.findElement(By.id("CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_TextBoxFirstName")).sendKeys("shanaz");
WebElement title=driver.findElement(By.id("CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_DropDownListTitle"));
Select sel3=new Select(title);
sel3.selectByVisibleText("MS");
driver.findElement(By.id("CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_TextBoxLastName")).sendKeys("fathima");
WebElement Nationality=driver.findElement(By.id("CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_DropDownListNationality"));
Select sel4=new Select(Nationality);
sel4.selectByVisibleText("INDIA");
driver.findElement(By.id("CONTROLGROUPREGISTERVIEW_MemberInputRegisterView_TextBoxAgentUserName")).sendKeys("humkobooo@gmail.com");
driver.findElement(By.id("CONTROLGROUPREGISTERVIEW_MemberInputRegisterView_PasswordFieldAgentPassword")).sendKeys("farooquhad");
driver.findElement(By.id("CONTROLGROUPREGISTERVIEW_MemberInputRegisterView_PasswordFieldPasswordConfirm")).sendKeys("farooquhad");
driver.findElement(By.id("CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_TextBoxStreetAddress1")).sendKeys("velachery");
driver.findElement(By.id("CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_TextBoxStreetAddress2")).sendKeys("velachery");
WebElement country=driver.findElement(By.id("CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_DropDownListCountry"));
Select sel5=new Select(country);
sel5.selectByVisibleText("INDIA");
driver.findElement(By.id("CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_TextBoxTownCity")).sendKeys("chennai");
driver.findElement(By.id("CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_TextBoxCountryCodeHomePhone")).sendKeys("91");
driver.findElement(By.id("CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_TextBoxFirstPhone")).sendKeys("1234556789");
driver.findElement(By.id("CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_TextBoxEmail")).sendKeys("humkobooo@gmail.com");
driver.findElement(By.id("CONTROLGROUPREGISTERVIEW_ButtonSubmit")).click();
	}

}

