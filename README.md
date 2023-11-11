# CalendarEvent
Configuration settings needed:
1.	Create a new Maven project and add below dependencies then right click on the project and select Maven Update project. Check that once project updated all these respective jars are downloaded and shown under Maven dependencies
<dependency>
    <groupId>org.seleniumhq.selenium</groupId>
    <artifactId>selenium-java</artifactId>
    <version>4.15.0</version>
</dependency>

<!-- https://mvnrepository.com/artifact/io.cucumber/cucumber-junit -->
<dependency>
    <groupId>io.cucumber</groupId>
    <artifactId>cucumber-junit</artifactId>
    <version>7.2.2</version>
</dependency>

<dependency>
    <groupId>io.cucumber</groupId>
    <artifactId>cucumber-jvm-deps</artifactId>
    <version>1.0.6</version>
</dependency>

<!-- https://mvnrepository.com/artifact/info.cukes/cucumber-java -->
<dependency>
    <groupId>io.cucumber</groupId>
    <artifactId>cucumber-java</artifactId>
    <version>7.2.2</version>
</dependency>
2.	Make sure the folder structure should be like below for this project and if not please do necessary changes
Src/main/java  To maintain all the common wrappers and generic methods
Src/main/resources  To maintain any generic code files
Src/test/java  To maintain helper files and step definitions
Src/test/resources  To maintain feature files, test data, config files etc
3.	Copy the helper files and step definition files under src/test/java under different packages
4.	Copy test runner file as well under src/test/java under different package
5.	Once all the code copied, right click on the test runner file and run as junit
Project details:
1.	DairyView_helper (src/test/java/HelperFiles) is the helper file where all the methods related to this calendar tiny app have been written
2.	DairyView_Stepdef (src/test/java/stepdefinitions) is the step definition file where the gherkin statements look into the relevant code for these steps
3.	Dairy_View.feature (src/test/resources/Features) will be having gherkin scenarios related to Feature 1 (US-1) in the given document. It will validate whether user is able to launch the app successfully and able to see an option to add events to calendar
4.	DairyAddEvent.feature (src/test/resources/Features) will have scenarios from Feature 2 (US-2) where user will be able to add an event for the past date which is already interview done (in default colour) and able to add 3 events for a future date where interviews are yet to happen in a specific colour
5.	DairyRemoveEvent.feature (src/test/resources/Features) will have scenarios from Feature 3 (US-3) where user will be able to delete the events added and make sure the events are deleted from app.
6.	Common Wrappers (src/main/java/Wrappers) will have the methods that are generic and specific to selenium
7.	Testrunner (src/test/java/TestRunner) will have test runner file with required cucumber options and defaulted to run all the features in the features folder currently
Sequence of steps followed:
![image](https://github.com/PriyankaKomanduri/CalendarEvent/assets/150553801/2c7c8edd-2c6e-4a5c-ba01-a16d12359698)
                          

