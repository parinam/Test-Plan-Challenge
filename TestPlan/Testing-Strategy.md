### Text Conversion
1. Manually test the feature branch to make sure all the combinations pass. (Banner text style, fonts and width)
    * Example: (Happy path)
        * actual_input = Plain text (TEST)
        * Font = Banner
        * Width = 100
        * expected_output = banner.txt and preview 
        ![alt text](../images/TEST.png "TEST")
2. If all the test cases pass, add the high quality test cases to automation suite.  
3. Text conversion automation:
    * UI Interaction - where users provide input text and match with preview results and banner.txt (downloadable file). The expected           output (preview result and downloadable file) can be stored as testdata in database or as a file in any common shared repo that is         accessible to developers and QA's.
   
    
