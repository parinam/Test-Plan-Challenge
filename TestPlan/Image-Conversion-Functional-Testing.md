1. Tests should be written in a way that they don’t break if input and output parameters match.
2. Tests can break if there were enhancements in the requirements later from business or refactoring of code by developers.
3. Text conversion automation:
    * Automated tests will have input files as part of test data for uploading file and compared with the output results stored as test       data.
    * Automated tests will have UI interaction of adding URLs and comparing with the output results stored as test data.
    * Adding of testdata is one time job but any new additions is easy to add.
 4. Nice to have for faster execution: 
    * The tests can run browser less (e.g HtmlUnitDriver). 
    * If developers add id’s on UI its much faster than css and xpaths.
 5. Test Steps for Pass Criteria:
    * Launch URL http://www.ascii-art-generator.org/
    * Select “Image to Monochrome Ascii Art” radio button
    * Enter the file - test (See 'Image Conversion' section under [Testing Strategy](./Testing-Strategy.md))
    * Choose file to upload or url (Supported file types: jpg, png, bmp, gif, jpeg)
    * Click on Start
    * Verify actual input matches with the expected output in preview
    * Verify banner.txt download functionality
    * Verify the downloaded file contents
    
@Test</br>
Public void imageConversionMonochrome()</br>
{</br>
//Launching the site and print out of the URL</br>
driver.get(“http:// ascii-art- generator.org”);</br>
String url = js.executeScript(“return document.URL;”).toString();</br>
System.out.println(“URL of the site = “+url);</br>

//Selecting "Image to Monochrome Ascii Art" radio button by finding element by css</br>
element = driver.find_element_by_id("ChooseFile")
element.send_keys("https://github.com/parinam/ascii-art-generator/blob/master/images/test.png")

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
//Launching the site and print out of the URL</br>
driver.get(“http:// ascii-art- generator.org”);</br>
String url = js.executeScript(“return document.URL;”).toString();</br>
System.out.println(“URL of the site = “+url);</br>

//Selecting "Text to Ascii Art Banner" radio button by finding element by css</br>
driver.findElement(webdriver.By.css(“radiobutton”).click();</br>

//send keys to element for empty text and find element by xpath</br>
driver.findElement.By.xpath(“//*[@type=\”banner_text\”]”)).sendkeys(“”);</br>

//Click on the Start and find element by id</br>
driver.findElement(webdriver.By.id(“Starts”)).click():</br>

//Error messages displayed if assertequal is not true or assertFalse for empty text

