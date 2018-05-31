# Selenium

`Framework`


https://drive.google.com/open?id=1_-ncwBJed2WomXqv9KVqZIRynadTraNR

****************************************************************
**Tips:**


* Interactuar con los objetos del contenedor:
```
getDriver().switchTo().frame(getDriver().findElement(By.tagName("iframe")));
```


* Interactuar con campo de fecha de lista desplegable:
```
public void inputDocumento(String documento) {

              inputDocumento.click();

       findBy("/html/body/form/div/div/div/div/div[2]/div[2]/div[2]/div/div[1]//li[text()='"+documento+"']").click();  
```


* Lista de elementos:
```
public void inputEstadoCivil(String EstadoCivil) {

              List<WebElement> lista = inputEstadoCivil.findElements(By.tagName("li"));

                     for (int i = 0; i < lista.size(); i++)

                     {

                           System.out.println(lista.get(i).getText());

                     if (lista.get(i).getText().equals(EstadoCivil)) {

                     lista.get(i).click();      

                     }

              } 
```

* Armar un xpath
```
//+nombre etiqueta(html-div-span)+[@atributo(class-id-xpath)="valor del atributo"]
ejm: //span[@class=\'as-login-close as-login-icon-close-circled\']
```
