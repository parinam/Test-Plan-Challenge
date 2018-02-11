1. Tests should be written in a way that they don’t break if input and output parameters match.
2. Tests can break if there were enhancements in the requirements later from business or refactoring of code by developers.
3. Text conversion automation:
    * UI Interaction - where users provide input text and match with preview results and banner.txt (downloadable file). The expected           output (preview result and downloadable file) can be stored as testdata in database or as a file in any common shared repo that is         accessible to developers and QA's.
    * Adding of testdata is one time job but any new additions is easy to add.
4. Test Steps for Pass Criteria:
    * Launch URL http://www.ascii-art-generator.org/
    * Select “Text to Ascii Art Banner” radio button
    * Enter the text - TEXT (See 'Text Conversion' section under [Testing Strategy](./TestPlan/Testing-Strategy.md))
    * Choose font from the drop down 
    * Click on Start
    * Verify actual input matches with the expected output in preview
    * Verify banner.txt download functionality
    * Verify the downloaded file contents
 5. Nice to have for faster execution: 
    * The tests can run browser less (e.g HtmlUnitDriver). 
    * If developers add id’s on UI its much faster than css and xpaths.
    
    
    
