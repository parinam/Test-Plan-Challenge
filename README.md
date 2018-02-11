# ASCII Art Generator Test Plan

## Assumptions
1. Developer code and all tests (unit, integration, functional, non functional) resides in one single shared repository
2. All automated tests use the infrastructure already in place (nightwatch.js)
3. All automated tests in continuous delivery development practice (Jenkins)
4. Load testing tool – Webload
5. Business can get Progress of tests (Pass/fail) for each feature from TestRail tool
6. Code Review process before merge is followed by developers and QA for tests
7. Following Agile Principles – after two weeks sprint, there is a release. Each squad/team member participates in sprint retrospective      and talks about what went well, what didn’t go well and any action items to improve the process in order to deliver high quality          product.

## Table of Contents
1. [Working Agreement for the Quality of the Product](./TestPlan/Working-Agreement.md)
2. [Environment and Browser](./TestPlan/Environment-Browser.md)
3. [Testing Procedures](./TestPlan/Testing-Procedures.md)
4. [Testing Strategy](./TestPlan/Testing-Strategy.md)
    * Text Conversion
    * [Text Conversion Functional Testing](./TestPlan/Text-Conversion-Functional-Testing.md)
    * Image Conversion
    * [Image Conversion Functional Testing](./TestPlan/Image-Conversion-Functional-Testing.md)
 5. [Non Functional Testing](./TestPlan/Non-Functional-Testing.md)
