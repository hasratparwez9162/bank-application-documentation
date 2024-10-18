# Bank Application

## Overview
This project consists of multiple services including User Service, Account Service,Loans Service and Cards Service. It uses Spring Boot for the backend and Vue.js for the frontend.

## Prerequisites
- Java 17 or higher
- Maven 3.6.0 or higher
- Node.js 14.x or higher
- npm 6.x or higher
- MySQL or any other SQL database

## Setup Instructions

### Step 1: Clone All Repositories

List of Repositories:
1. api-gateway
2. User-Service
3. Banking-UI
4. config-repo
5. loan-service
6. account-service
7. card-service
8. notification-server
9. core
10. keycloak-25.0.4
11. config-server
12. service-registry

Clone each repository one by one:
```sh
git clone https://github.com/hasratparwez9162/api-gateway.git
git clone https://github.com/hasratparwez9162/User-Service.git
git clone https://github.com/hasratparwez9162/Banking-UI.git
git clone https://github.com/hasratparwez9162/config-repo.git
git clone https://github.com/hasratparwez9162/loan-service.git
git clone https://github.com/hasratparwez9162/account-service.git
git clone https://github.com/hasratparwez9162/card-service.git
git clone https://github.com/hasratparwez9162/notification-server.git
git clone https://github.com/hasratparwez9162/core.git
git clone https://github.com/hasratparwez9162/keycloak-25.0.4.git
git clone https://github.com/hasratparwez9162/config-server.git
git clone https://github.com/hasratparwez9162/service-registry.git
```
### Step 2: Database Setup
### Create a database:  
#### CREATE DATABASE bank_app;
- Update the database configuration in application.properties for each service:

```sh
spring.datasource.url=jdbc:mysql://localhost:3306/bank_app
spring.datasource.username=your-username
spring.datasource.password=your-password
```
Note: You can use the same database for all services or create a separate database for each service.
### Step 2: Maven Build & Install
1. Build and install the core module first: 
```sh
cd core
mvn clean install
cd ..
```
2. Build and install the remaining services:
```sh
cd api-gateway
mvn clean install
cd ..

cd User-Service
mvn clean install
cd ..

cd loan-service
mvn clean install
cd ..

cd account-service
mvn clean install
cd ..

cd card-service
mvn clean install
cd ..

cd notification-server
mvn clean install
cd ..

cd config-server
mvn clean install
cd ..

cd service-registry
mvn clean install
cd ..
```
### Step 3: keycloak Setup
1. Go to the keycloak-25.0.4 folder and Read the README.md file for keycloak setup instructions.

### Step 4: Kafka Setup
1. Run docker-compose
2. file provided in core module to start Zookeeper and kafka.

### Step 5: Run the Services

1. Run the service-registry first
2. Run the config-server
3. Run the remaining services in any order

### Step 6: Run the Banking-UI
1. Go to the Banking-UI folder
2. Run the following commands:
```sh
npm install
npm run serve
```
3. Open the browser and go to http://localhost:8085 

Good to go! You can now use the Bank Application.