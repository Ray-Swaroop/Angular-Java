# AngularJava

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 6.1.2.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).

#Refrence
https://www.evoketechnologies.com/blog/integrate-angular-spring-boot-restful-api/

#Check for the repo Angular-Java-Connect for the SpringBoot connection with Angular

Up to now, Angular4-Client and Spring Boot server worked independently on ports 8080 and 4200. The goal of the below integration is to ensure that client at 4200 will proxy any API requests to the server.

Steps to Follow

Create a file proxy.conf.json under project angular4-client folder with content:
{
"/api":{
"target": "http://localhost:8080",
"secure": false
}
}

Edit package.json file for start script:

"start": "ng serve --proxy-config proxy.conf.json",

Build and run Spring Boot application with below command:
mvn clean install
mvn spring-boot:run

Build and Run Angular4-client with below commands

ng build
npm start 

Type the URL http://localhost:4200 into your browser and you are all set
