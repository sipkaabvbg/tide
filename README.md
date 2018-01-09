# Tide Non-blocking Backend Application 
The Tide Non-blocking Backend Application is created to handle requests of mobile devices 
in the conditions of high load of multiple requests.

## Build and Run

Project should be build and run using Java 1.8 or above.

1. To run the application you must initially start MySQL database and create a schema whit name "tide"

2. Open the "application.properties" file and set your own configurations for the
       database connection.
    
3. Build with Maven "mvn clean install"  
    
4. Change directory to "../tide.rest.mobile/target/"
     
5. Execute in the terminal "java -jar tide.rest.mobile-1.0.0-SNAPSHOT.jar " 
    
Alternatively run "mvn spring-boot:run" from command line or IDE or execute "com.tide.mobile.Application.main()" from within IDE.

## Documentation of the REST API
Once the service is up and running the documentation of the REST API can be accessed at:
    
* API documentation JSON [http://localhost:8080/v2/api-docs/](http://localhost:8080/v2/api-docs)
* API documentation WEB UI [http://localhost:8080/swagger-ui.html](http://localhost:8080/swagger-ui.html)

## Used technology-Spring Boot with Swagger + JPA + Hibernate + MySQL 
Non-blocking RESTful web service with Spring Boot, JPA, Hibernate, MySQL and Swagger.
API documentation is generated using Swagger.

## Design
### API
The project contains an API package "com.tide.mobile.api" with all the interfaces describing the main application functionality.
### Implementation

The implementation of functionality is found in the following packages:

-com.tide.mobile -this package is the primary launch class of the application

-com.tide.mobile.controller -this package contains the controllers in the application

-com.tide.mobile.config -this package contains the configuration class

-com.tide.mobile.dao -this package contains the DAO classes

-com.tide.mobile.domain -this package are the classes describing the application domain

-com.tide.test -this package contains classes running tests

##Test scenarios

To run tests the application must be running.
The following test scenarios are performed:

1 creating a user, 2 creating a feature, 3 adding a feature to user, 4 checking all user's features.

Automatic tests you can run from IDE with execute "com.tide.test.TideMobileTest.test ()"

