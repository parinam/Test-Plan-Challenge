## Testing at all levels:
To achieve continuous delivery, quality should be intact at every level.
![alt text](../images/testing-at-all-levels.png "testing-at-all-levels")

### Unit Testing
1. Method level testing done by developers on their local dev machines.
2. UI unit coverage can be evaluated from tools like Karma.
3. API unit coverage can be evaluated from tools like Sonar.
4. Developers test data is limited and the data is mocked.
5. Jenkins build fails if any unit tests fail.

### Functional testing –
1. Feature testing done by QA’s or developers on QA env or local machines. (Ideal situation is QA's testing feature branch in QA env)
2. Making sure the functionality of the feature is intact as per the requirement discussed during early phase
3. Manual testing of the feature if the automated tests were not written in the same sprint
4. Automated tests feature/regression run as part of CI to make sure other functionalities are working as expected
5. If the automated tests build failed, an alert is sent to the developers and QA’s to look for the test case or cases that failed with      the new feature development.

### Performance testing –
1. Feature performance testing done by QA’s or developers on local or QA env
- Display results through charts to stakeholders and business
- This does not replicate the real prod scenario, so it may be
approx. results that can raise an alarm before the feature is
released
