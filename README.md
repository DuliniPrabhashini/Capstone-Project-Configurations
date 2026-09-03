# Capstone-Project-Configurations

This repository contains the centralized configuration files used by the Capstone Project microservices.

The project uses **Spring Cloud Config Server** to load application configuration from this repository. This keeps configuration separate from the application source code and makes it easier to change settings when deploying the system to the cloud.

## Project Structure

```text
Capstone-Project-Configurations/
│
├── application.yaml
├── application-dev.yaml
│
├── platform/
│   ├── api-gateway.yaml
│   ├── service-registry.yaml
│   └── service-registry-dev.yaml
│
└── services/
    ├── student-service.yaml
    ├── student-service-dev.yaml
    ├── program-service.yaml
    ├── program-service-dev.yaml
    ├── enrollment-service.yaml
    └── enrollment-service-dev.yaml
```

## Configuration

### Platform

Configuration for:

* API Gateway
* Service Registry
* Config Server

### Services

Configuration for:

* Student Service
* Program Service
* Enrollment Service

## Local Development

Development specific settings are maintained in the `*-dev.yaml` files.

Database and service URLs are defined in the corresponding configuration files.

## Cloud Deployment

When deploying to the cloud, the development values should be changed to the appropriate cloud addresses.

Database connection details should also be updated for the cloud environment.
