# Unit/Integration Testing using java-restaurants/restaurants-testing

1. create src/test/java folder
2. create src/test/resources
3. For intellij Idea, to define automatic test folder

	a. File->Project Structure->Modules->Source Folders
		* select test/java, right-click-> select "test" folder.
		* select test/resources, right-click->select "test resources".
4. Add unit testing into pom.xml, along with spring-boot-starter-test
	* junit-jupiter-api
5. Add rest api testing into pom.xml
	* spring-mock-mvc
6. Change in-memory h2 database to mocked database
	* test/resources->spring.datasource.url=jdbc:h2:mem:mockeddb
7. Create java main class and seed data for testing in test/java.
8. > Majority of unit testing, will be done on service implementation.  
	* assertEqual
	> Integration testing will be done on controller
		* given().when().then() -> given then, when expect, then result.
	> No testing on repos because there is no nee for database testing.
9. > For intellij Idea, goto serviceimpl, right-click->select test to create jnit4 test file.
	> Eclipse, create junit4 test file with filename suffix "test" in test folder.
	> create setup() and teardown() function.
10. Unit testing - 
	* stub - fake a return of a method
	* mock -> create mocked seed data, or faking it somehow. 
11. Harding thing to do, is to decide what to test.
	* try to write code that test as much code as possible, or test method that cover as much area as possible.
12. Run "test with coverage", on Intellij Idea->right-click-> select "run test with coverage".

