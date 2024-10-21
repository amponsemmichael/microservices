# Microservices & Service Discovery with Eureka

## Project Overview
This repository demonstrates the implementation of service discovery in a microservices architecture using Spring Cloud Netflix Eureka. It includes a Eureka server and multiple microservices that register with Eureka and perform service discovery.

## Components

1. **Eureka Server**: Central service registry
2. **Microservice A**: Example microservice that registers with Eureka
3. **Microservice B**: Another example microservice that registers with Eureka and discovers Microservice A

## Prerequisites

- Java JDK 17 or later
- Maven 3.6 or later
- Git

## Getting Started

### 1. Clone the Repository

```bash

cd service-registry
```

### 2. Build the Projects

```bash
mvn clean package
```

### 3. Run the Eureka Server

```bash
java -jar eureka-server/target/eureka-server-0.0.1-SNAPSHOT.jar
```

The Eureka dashboard will be available at `http://localhost:8761`

### 4. Run Microservice A

```bash
java -jar microservice-a/target/microservice-a-0.0.1-SNAPSHOT.jar
```

### 5. Run Microservice B

```bash
java -jar microservice-b/target/microservice-b-0.0.1-SNAPSHOT.jar
```

## Testing Service Discovery

1. Access Microservice B's endpoint that calls Microservice A:
   ```
   http://localhost:8082/call-service-a
   ```

2. Check the Eureka dashboard to see registered services:
   ```
   http://localhost:8761
   ```

3. Stop and start services to observe dynamic service registration and discovery.

## Project Structure

```
microservices-service-discovery/
│
├── eureka-server/
│   └── src/
│       └── main/
│           ├── java/
│           └── resources/
│
├── microservice-a/
│   └── src/
│       └── main/
│           ├── java/
│           └── resources/
│
├── microservice-b/
│   └── src/
│       └── main/
│           ├── java/
│           └── resources/
│
├── docs/
│   └── service-discovery-eureka.pdf
│
└── README.md
```

## Key Features

- Eureka server setup and configuration
- Microservices registration with Eureka
- Client-side service discovery implementation
- Demonstration of service discovery resilience

## Documentation

For a detailed explanation of service discovery concepts and Eureka configuration, refer to the `docs/service-discovery-eureka.pdf` file in this repository.

## Video Demonstration

A video demonstration of the running system, including the Eureka server dashboard and service discovery in action, is available [here](link-to-your-loom-video).

## Contributing

This project is part of a learning exercise. While it's not open for direct contributions, feedback and suggestions are welcome. Please open an issue in the repository if you have any questions or comments.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

---

For any queries regarding this project, please contact [Your Name] at [Your Email].
