"Komment Demo Task"
Komment Demo Task
# Connect-CRM Spring Boot Web App

 This project is a full-stack web application built using modern Java(SpringBoot). <br>
 The application is a Customer Relationship Management (CRM) system for managing contacts. It features:

- A log-in screen to restrict access.

- A responsive layout with side navigation that works on desktop and mobile.

- A database for persistent data storage.

- A list view that can be sorted and filtered.

- A form to edit and add contacts.

- A dashboard view.

- Cloud deployment.

- Application installation on mobile and desktop.



## Running the application

The project is a standard Maven project. To run it from the command line,
type `mvnw` (Windows), or `./mvnw` (Mac & Linux), then open
http://localhost:8080 in your browser.

You can also import the project to your IDE of choice as you would with any
Maven project.(Eclipse, IntelliJ IDEA, NetBeans, and VS Code).

## Deploying to Production

To create a production build, call `mvnw clean package -Pproduction` (Windows),
or `./mvnw clean package -Pproduction` (Mac & Linux).
This will build a JAR file with all the dependencies and front-end resources,
ready to be deployed. The file can be found in the `target` folder after the build completes.

Once the JAR file is built, you can run it using
`java -jar target/connectcrm-1.0-SNAPSHOT.jar`

## Project structure

- `MainLayout.java` in `src/main/java` contains the navigation setup (i.e., the
  side/top bar and the main menu). 
- `views` package in `src/main/java` contains the server-side Java views of your application.
- `views` folder in `frontend/` contains the client-side JavaScript views of your application.
- `themes` folder in `frontend/` contains the custom CSS styles.


## Deploying using Docker

To build the Dockerized version of the project, run

```
mvn clean package -Pproduction
docker build . -t connectcrm:latest
```

Once the Docker image is correctly built, you can test it locally using

```
docker run -p 8080:8080 connectcrm:latest
```
