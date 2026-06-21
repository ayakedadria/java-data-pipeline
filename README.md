# Production Java Data Pipeline
Real-time sales analytics pipeline using Java, Spring Boot, Kafka, PostgreSQL, Docker.
Run:
docker-compose up -d
mvn spring-boot:run
Real-Time Sales Analytics Pipeline (Java, Kafka, Spring Boot)
It demonstrates how real-time event streams are processed and persisted using a scalable backend architecture.

System Arcitechture:

A[Sales Event Producer<br/>Spring Boot Service] --> B[Apache Kafka<br/>sales-events topic]

B --> C[Consumer Service<br/>Spring Boot]

C --> D[PostgreSQL Database<br/>Persistent Storage]

D --> E[Analytics / Reporting Layer]
Architecture Overview

The system is built around an event-driven pipeline:

The Producer Service publishes sales events to Kafka
Kafka acts as the central event streaming backbone
The Consumer Service processes and transforms events
PostgreSQL stores structured, queryable sales data
The system is designed for horizontal scalability and service isolation
Tech Stack
Java 17
Spring Boot
Apache Kafka
PostgreSQL
Docker / Docker Compose
Maven
Project Structure
production-java-data-pipeline/
├── producer-service/      # Event producer (Kafka publisher)
├── consumer-service/      # Event consumer (processor + DB writer)
├── common/               # Shared DTOs and domain models
├── docker-compose.yml    # Local infrastructure stack
├── Dockerfile            # Service containerization (prod-ready)
└── pom.xml               # Multi-module build
