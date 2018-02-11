## Testing at all levels:
To achieve continuous delivery, quality should be intact at every level.
![alt text](../images/testing-at-all-levels.png "testing-at-all-levels")

### Unit Testing
1. Method level testing done by developers on their local dev machines.
2. UI unit coverage can be evaluated from tools like Karma.
3. API unit coverage can be evaluated from tools like Sonar.
4. Developers test data is limited and the data is mocked.
5. Jenkins build fails if any unit tests fail.
