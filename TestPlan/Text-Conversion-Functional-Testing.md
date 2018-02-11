1. Tests should be written in a way that they don’t break if input and output parameters match.
2. Tests can break if there were enhancements in the requirements later from business or refactoring of code by developers.
3. Text conversion automation:
    * UI Interaction - where users provide input text and match with preview results and banner.txt (downloadable file). The expected           output (preview result and downloadable file) can be stored as testdata in database or as a file in any common shared repo that is         accessible to developers and QA's.
    * Adding of testdata is one time job but any new additions is easy to add.
 4. Nice to have for faster execution: 
    * The tests can run browser less (e.g HtmlUnitDriver). 
    * If developers add id’s on UI its much faster than css and xpaths.
 5. Test Steps for Pass Criteria:
    * Launch URL http://www.ascii-art-generator.org/
    * Select “Text to Ascii Art Banner” radio button
    * Enter the text - TEXT (See 'Text Conversion' section under [Testing Strategy](./Testing-Strategy.md))
    * Choose font from the drop down 
    * Click on Start
    * Verify actual input matches with the expected output in preview
    * Verify banner.txt download functionality
    * Verify the downloaded file contents
    
@Test</br>
Public void textConversionPositive()</br>
{</br>
//Launching the site and print out of the URL</br>
driver.get(“http:// ascii-art- generator.org”);</br>
String url = js.executeScript(“return document.URL;”).toString();</br>
System.out.println(“URL of the site = “+url);</br>

//Selecting "Text to Ascii Art Banner" radio button by finding element by css</br>
driver.findElement(webdriver.By.css(“radiobutton”).click();</br>

//send keys to element to enter text and find element by xpath</br>
driver.findElement.By.xpath(“//*[@type=\”banner_text\”]”)).sendkeys(“TEST);</br>

//Click on the Start and find element by id</br>
driver.findElement(webdriver.By.id(“Starts”)).click():</br>

//assert equal to true</br>
driver.findElement(By.id(‘previewtext’)).getText().then(textValue={assert.equal(‘banner_text’,previewtext)</br>

//Download file and verify contents</br>
Assert.equal(dowloadedfile==expectedoutputfile, “check two files are equal”);</br>
driver.quit();</br>
}
    
6. Test Steps for Fail Criteria:
    * Launch URL http://www.ascii-art-generator.org/
    * Select “Text to Ascii Art Banner” radio button
    * Leave Banner text section empty (See 'Text Conversion Example 6' section under [Testing Strategy](./Testing-Strategy.md))
    * Choose font from the drop down 
    * Click on Start
    * Verify error message "Please enter a text for your banner."
 
@Test</br>
Public void textConversionNegative()</br>
{</br>
//Launching the site</br>
driver.get(“http:// ascii-art- generator.org”);</br>
String url = js.executeScript(“return document.URL;”).toString();</br>
System.out.println(“URL of the site = “+url);</br>
//Selecting text to ascii banner radio button</br>
driver.findElement(webdriver.By.css(“radiobutton”).click();</br>
//send keys to element to enter text</br>
driver.findElement.By.xpath(“//*[@type=\”banner_text\”]”)).sendkeys(“”);</br>
//Click on the Start
driver.findElement(webdriver.By.id(“Starts”)).click():</br>
//Error messages displayed</br>

    
