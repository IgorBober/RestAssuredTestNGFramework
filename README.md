# REST Assured API Automation Framework.

This is a project for REST API Automation testing of Spotify application.

## Used Tools/Technologies:
* Rest Assured
* Java (15.02)
* TestNG
* Maven
* Allure Reports
* Hamcrest
* Jackson API
* Lombok

## Key points:
- Framework is scalable and extensible
- Reusable Rest Assured API requests
- Reusable Rest Assured specifications
- For Serialization and De-serialization are used POJO classes
- Lombok for reducing boilerplate code
- Builder pattern for "setter" methods in POJOs
- Automated access_token renewal
- Automate positive and negative scenarios
- Singleton Design Pattern
- Separation of API layer from test layer
- Integrated with Allure Reporting
- Support parallel execution
- Implemented tests running using Maven in the terminal
- Configured running of auto-tests in Jenkins CI system.

## Description of a Project Structure

### src/test/java
### com.spotify.oauth2
- api ->> applicationApi ->> PlaylistApi - (Consists of common methods for Playlist API)
- api ->> Rest Resource - (Consists of reusable API requests throughout the application)
- api ->> Route - (Stores base path parameters for requests)
- api ->> SpecBuilder - (A class for Request/Response specifications)
- api ->> StatusCode - (An Enum for storing possible status codes with appropriates messages)
- api ->> TokenManager - (A class for checking the state of a token and renew it)


- pojo ->> (Classes for representing a JSON object)


- tests ->> BaseTest (A class for implementing "beforeMethod" method)
- tests ->> Playlist (This is main class for tests)


- utils ->> ConfigLoader (A class for loading the configuration properties)
- utils ->> DataLoader (A class for loading some important data for tests)
- utils ->> FakerUtils (A class for generating fake data for creation entities)
- utils ->> PropertyUtils (A class for loading and reading the configuration properties)


- resources ->> allure.properties (A file for managing Allure reporting)
- resources ->> config.properties (A file for storing the configuration properties)
- resources ->> data.properties (A file for storing some important data for tests)

