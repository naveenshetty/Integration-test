# Integration Tests - [Smava](www.smava.de)

Integration test project based on JBehave and Selenium

## Project Overview 

1. src/test/java/de/smava/int_test/Stories.java is the entry-point that JBehave uses to run the stories.
2. src/test/java/stories contains the stories run by JBehave via Stories.java.
3. src/test/java/de/smava/int_test/steps/Steps.java contains the steps mapped to the textual steps.
4. src/test/java/de/smava/int_test/pages contains the Java page-objects (SmavaHome.java, LoanDetailsResult.java and ScoreCompassHome.java) used by steps to abstract in a more manageable and maintainable way the interaction with the web pages via Selenium WebDriver.
5. src/test/java/resources/smavatest-steps.xml contains the Spring configuration for composition the steps


## Prerequisites

* JDK 8
* Maven 3
* Firefox 25 or later


## Configuration

Make sure that:
* JAVA\_HOME and M2\_HOME system variables are properly set.
* Directory of Firefox binary is in your $PATH.


## Library and version used

* selenium-java: 2.53.1
* jbehave-core:4.0.5
* jbehave-web:3.6-beta-2
* jbehave-site:3.3
* fluent-selenium:1.16.1
* selenium-common:2.0b1
* guava:11.0.1
* hamcrest:1.1
* junit:4.8.2


## Adding a new user story

Create a new JBehave story under src/test/java/stories directory.


## Running the stories

The below command will run the build and causes the Firefox to open and run the tests:

    mvn clean install

The below command can be used to run a single story:

    mvn clean install -DstoryFilter=loanSelectionFromSmavaPage


## Reporting

After each run, a new report (reports.html) will be created under the directory target/jbehave/view.