### Text Conversion
1. Manually test the feature branch to make sure all the combinations pass. (Banner text style, fonts and width)
    * Example 1: (Happy path)
        * actual_input = Plain text (TEST)
        * Font = Banner
        * Width = 100
        * expected_output = banner.txt and preview 
        ![alt text](../images/TEST.png "TEST")
        
    * Example 2: 
        * actual_input = Plain text with numbers (TEST12)
        * Font = Banner
        * Width = 400
        * expected_output = banner1.txt and preview 
        
     * Example 3: 
        * actual_input = Combination of text, numbers and special characters  (TEST12*&^)
        * Font = Banner
        * Width = 80
        * expected_output = banner3.txt and preview 
    
    * Example 4: 
        * actual_input = Numbers  (12345)
        * Font = Banner
        * Width = 250
        * expected_output = banner4.txt and preview 
        
     * Example 5: 
        * actual_input = Small text  (text)
        * Font = Banner
        * Width = 100
        * expected_output = banner5.txt and preview 
        
*Note - Repeat above test cases for all the font options (big,block,bubble,lean,mini,script,shadow,slant,standard).
        
2. If all the test cases pass, add the high quality test cases to automation suite that runs in continuous integration development            practice.
