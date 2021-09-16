DESAFIOQA_TestSeleniumJUnit Desafio proposto pelo programa de Extensão da Fábrica de Software. Projeto de automação web e Selenium e JUnit. Verificação de valores nos campos pedidos com atualizações de Asserts, em um site de teste ("https://testpages.herokuapp.com/styled/basic-html-form-test.html") Utilizamos o WebDriver.


import io.github.bonigarcia.wdm.WebDriverManager;
import org.junit.After;
import org.junit.Assert;
import org.junit.Before;
import org.junit.Test;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;

public class desafio{

    private WebDriver driver;

    @Before
    public void desafio() {
        WebDriverManager.chromedriver().setup();
        this.driver = new ChromeDriver();
        driver.get("https://testpages.herokuapp.com/styled/basic-html-form-test.html");

    }


    @Test
    public void fluxoPrincipal(){
        driver.findElement(By.name("username")).sendKeys("Felipe");
        driver.findElement(By.name("password")).sendKeys("123456");
    WebElement commentsBox = driver.findElement(By.name("comments"));

    commentsBox.clear();
    commentsBox.sendKeys("Comments...");


        driver.findElement(By.xpath("//input[@value='cb3']")).click();
        driver.findElement(By.xpath("//input[@value='cb1']")).click();

       driver.findElement(By.xpath("//input[@value='submit'1")).click();

       //Validações


        Assert.assertEquals("Felipe", driver.findElement((By.id("-valueusername")).getText();
        Assert.assertEquals("123456", driver.findElement((By.id("-valuepassword")).getText();
        Assert.assertEquals("Comments...", driver.findElement((By.id("-valuecomments")).getText();


        Assert.assertEquals("cb3", driver.findElement(By.id("-valuecheckboxs0")).getText();
        Assert.assertEquals("cb1", driver.findElement(By.id("-valuecheckboxs0")).getText();


















    }



    @After
    public void fim(){
    driver.quit()



    }




}
