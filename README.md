# Spring Microservices Project

Este proyecto es una introducción al desarrollo de microservicios utilizando Spring Boot y Spring Cloud. El objetivo es aprender y explorar la arquitectura de microservicios mediante la implementación de un sistema simple que incluye varios servicios independientes que interactúan entre sí.

## Características del Proyecto

- **microservice-config**: Servicio de configuración centralizada para gestionar configuraciones compartidas entre los microservicios.
- **microservice-course**: Microservicio para la gestión de cursos.
- **microservice-eureka**: Servidor Eureka para el descubrimiento de servicios.
- **microservice-gateway**: API Gateway para manejar solicitudes hacia los microservicios.
- **microservice-student**: Microservicio para la gestión de estudiantes.

## Tecnologías Utilizadas

- Java 17
- Spring Boot
- Spring Cloud (Eureka, Config Server, Gateway)
- Maven

## Requisitos Previos

- JDK 17 o superior
- Maven 3.8+
- IDE como IntelliJ IDEA o Eclipse
- Docker (opcional, para ejecutar servicios en contenedores)

## Estructura del Proyecto

```
SpringMicroservices/
├── microservice-config
├── microservice-course
├── microservice-eureka
├── microservice-gateway
├── microservice-student
└── pom.xml
```

## Configuración y Ejecución

### 1. Clonar el repositorio

```bash
git clone <URL-del-repositorio>
cd SpringMicroservices
```

### 2. Iniciar el Config Server

```bash
cd microservice-config
mvn spring-boot:run
```

### 3. Iniciar el Servidor Eureka

```bash
cd ../microservice-eureka
mvn spring-boot:run
```

### 4. Iniciar el API Gateway

```bash
cd ../microservice-gateway
mvn spring-boot:run
```

### 5. Iniciar los Microservicios

```bash
cd ../microservice-course
mvn spring-boot:run

cd ../microservice-student
mvn spring-boot:run
```

## Endpoints Principales

- **Eureka Dashboard**: `http://localhost:8761`
- **API Gateway**: `http://localhost:8080`
- **Microservicio de Cursos**: `http://localhost:8080/course`
- **Microservicio de Estudiantes**: `http://localhost:8080/student`
