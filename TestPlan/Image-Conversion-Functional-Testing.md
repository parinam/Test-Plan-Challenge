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
    * Choose file to upload or url (Supported file types: jpg, png, bmp, gif, jpeg) (See 'Image Conversion' section under [Testing Strategy](./Testing-Strategy.md))
    * Click on Start
    * Verify actual input matches with the expected output in preview
    * Verify banner.txt download functionality
    * Verify the downloaded file contents
    
@Test</br>
Public void imageConversionMonochromeFileUpload()</br>
{</br>
//Launching the site and print out of the URL</br>
driver.get(“http:// ascii-art- generator.org”);</br>
String url = js.executeScript(“return document.URL;”).toString();</br>
System.out.println(“URL of the site = “+url);</br>

//Selecting "Image to Monochrome Ascii Art" radio button by finding element by css</br>
element = driver.find_element_by_id("ChooseFile")
element.send_keys("D:\test.png")

//Click on the Start and find element by id</br>
driver.findElement(webdriver.By.id(“Starts”)).click():</br>

//assert equal to true</br>
driver.findElement(By.id(‘previewtext’)).getText().then(textValue={assert.equal(‘test.png’,previewtext)</br>

//Download file and verify contents https://github.com/parinam/ascii-art-generator/blob/master/images/test_output.png</br>
Assert.equal(dowloadedfile==expectedoutputfile, “check two files are equal”);</br>
driver.quit();</br>
}

@Test</br>
Public void imageConversionMonochromeURL()</br>
{</br>
//Launching the site and print out of the URL</br>
driver.get(“http:// ascii-art- generator.org”);</br>
String url = js.executeScript(“return document.URL;”).toString();</br>
System.out.println(“URL of the site = “+url);</br>

//send keys to element to enter text and find element by xpath
driver.findElement.By.xpath(“//*[@type=\”banner_text\”]”)).sendkeys("https://github.com/parinam/ascii-art-generator/blob/master/images/test.png");

//Click on the Start and find element by id</br>
driver.findElement(webdriver.By.id(“Starts”)).click():</br>

//assert equal to true</br>
driver.findElement(By.id(‘previewtext’)).getText().then(textValue={assert.equal(‘test.png’,previewtext)</br>

//Download file and verify contents</br>
Assert.equal(dowloadedfile==expectedoutputfile, “check two files are equal”);</br>
driver.quit();</br>
}

*Note similar above test cases can be written for Color File Upload and Color URL. One extra step to add is selectedt output format and validate if the uploaded files mataches with selected output 

6. Test Steps for Fail Criteria:
    * Launch URL http://www.ascii-art-generator.org/
    * Select “Image to Monochrome Ascii Art” radio button
    * Do not choose a file to upload or enter URL
    * Click on Start
    * Verify error message
 
@Test</br>
Public void imageConversionMonochromeFileUploadEmpty()</br>
{</br>
//Launching the site and print out of the URL</br>
driver.get(“http:// ascii-art- generator.org”);</br>
String url = js.executeScript(“return document.URL;”).toString();</br>
System.out.println(“URL of the site = “+url);</br>

//Selecting "Image to Monochrome Ascii Art" radio button by finding element by css</br>
element = driver.find_element_by_id("ChooseFile")
element.send_keys("")

//Click on the Start and find element by id</br>
driver.findElement(webdriver.By.id(“Starts”)).click():</br>

//Error messages displayed if assertequal is not true or assertFalse for empty file or no URL

driver.quit();</br>
}

@Test</br>
Public void imageConversionMonochromeEmptyURL()</br>
{</br>
//Launching the site and print out of the URL</br>
driver.get(“http:// ascii-art- generator.org”);</br>
String url = js.executeScript(“return document.URL;”).toString();</br>
System.out.println(“URL of the site = “+url);</br>

//send keys to element to enter text and find element by xpath
driver.findElement.By.xpath(“//*[@type=\”banner_text\”]”)).sendkeys("");

//Click on the Start and find element by id</br>
driver.findElement(webdriver.By.id(“Starts”)).click():</br>

//Error messages displayed if assertequal is not true or assertFalse for no URL
driver.quit();</br>
}

@Test</br>
Public void imageConversionMonochromeFileUploadLargeSize()</br>
{</br>
//Launching the site and print out of the URL</br>
driver.get(“http:// ascii-art- generator.org”);</br>
String url = js.executeScript(“return document.URL;”).toString();</br>
System.out.println(“URL of the site = “+url);</br>

//Selecting "Image to Monochrome Ascii Art" radio button by finding element by css</br>
element = driver.find_element_by_id("ChooseFile")
element.send_keys("D:/xyz.png")

//Click on the Start and find element by id</br>
driver.findElement(webdriver.By.id(“Starts”)).click():</br>

//Error messages displayed if assertequal is not true or assertFalse for size > 5 MB

driver.quit();</br>
}

@Test</br>
Public void imageConversionMonochromeInvalidURL()</br>
{</br>
//Launching the site and print out of the URL</br>
driver.get(“http:// ascii-art- generator.org”);</br>
String url = js.executeScript(“return document.URL;”).toString();</br>
System.out.println(“URL of the site = “+url);</br>

//send keys to element to enter text and find element by xpath
driver.findElement.By.xpath(“//*[@type=\”banner_text\”]”)).sendkeys("http://xyz.co");

//Click on the Start and find element by id</br>
driver.findElement(webdriver.By.id(“Starts”)).click():</br>

//Error messages displayed if assertequal is not true or assertFalse if the URL does not contains .com, .net etc. This can be defined earlier by making sure the URL contains some elements or store in the database as test data to match with that URL.

driver.quit();</br>
}

*Note similar above test cases can be written for Color File Upload and Color URL. One extra step to add is selected output format and validate if the uploaded files mataches with selected output 

