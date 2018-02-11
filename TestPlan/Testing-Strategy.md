### Text Conversion
1. Manually test the feature branch to make sure all the combinations pass. (Banner text style, fonts and width)
    * Example 1: (Happy path)
        * actual_input = Plain text (TEST)
        * Font = Banner
        * Width = 100
        * expected_output = banner.txt and preview 
        ![alt text](../images/TEST.png "TEST")
        
    * Example 2: (Happy path)
        * actual_input = Plain text with numbers (TEST12)
        * Font = Banner
        * Width = 400
        * expected_output = banner1.txt and preview 
        
     * Example 3: (Happy path)
        * actual_input = Combination of text, numbers and special characters  (TEST12*&^)
        * Font = Banner
        * Width = 80
        * expected_output = banner3.txt and preview 
    
    * Example 4: (Happy path)
        * actual_input = Numbers  (12345)
        * Font = Banner
        * Width = 250
        * expected_output = banner4.txt and preview 
        
     * Example 5: (Happy path)
        * actual_input = Small text  (text)
        * Font = Banner
        * Width = 100
        * expected_output = banner5.txt and preview 
        
*Note - Repeat above test cases for all the font options (big,block,bubble,lean,mini,script,shadow,slant,standard).
  
   * Example 6: (Negative path)
        * actual_input = Empty
        * Font = Banner
        * Width = 100
        * expected_output = Error Message
        
   * Example 8: (Negative path)
        * actual_input = Max characters
        * Font = Banner
        * Width = 100
        * expected_output = Error Message
        
    * Example 9: (Negative path)
        * actual_input = Max characters
        * Font = None
        * Width = 100
        * expected_output = Error Message
2. If all the test cases pass, add the high quality test cases to automation suite that runs in continuous integration development            practice.

## Image Conversion
1. Manually test the feature branch to make sure all the combinations pass (Upload images with supported file types = jpg, png, bmp,        gif, jpeg)
2. Manually test image conversion by entering URL of images with supported file types = jpg, png, bmp, gif, jpeg and width range (40-      800)
3. Manually test image conversion by uploading or entering URL and selecting the supported output format.
  
  * Example 1: (Happy path)
        * actual_input = File (test)
         ![alt text](../images/test.png "test")
        * Format = png
        * Width = 100
        * expected_output = test.txt and preview 
        ![alt text](../images/test_output.png "test")
        
   * Example 2: (Happy path)
        * actual_input = URL
        * Format = jpg
        * Width = 100
        * expected_output = test.txt and preview 
 
*Note - Repeat above test cases for all the font options ( jpg, png, bmp, gif, jpeg etc).
  
  * Example 3: (Negative path)
        * actual_input = No file
        * Width = 100
        * expected_output = Error Message
      
   * Example 4: (Negative path)
        * actual_input = URL
        * Format = jpg
        * Width = None
        * expected_output = No image
 
