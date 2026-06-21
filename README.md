# Production Java Data Pipeline
Real-time sales analytics pipeline using Java, Spring Boot, Kafka, PostgreSQL, Docker.
Run:
docker-compose up -d
mvn spring-boot:run
Summary

This project simulates a real-world event streaming architecture where sales events are generated, streamed through Kafka, processed by a consumer service, and persisted in PostgreSQL for analytics,reflecting patterns used in modern distributed systems for e-commerce, fintech, and data platforms.

Architecture
Producer (Spring Boot)
        |
        v
Apache Kafka (Event Bus)
        |
        v
Consumer (Spring Boot)
        |
        v
PostgreSQL (Analytics Store)

Project Structure
production-java-data-pipeline/
├── producer-service/      # Event producer (Kafka publisher)
├── consumer-service/      # Event consumer (processor + DB writer)
├── common/               # Shared DTOs and domain models
├── docker-compose.yml    # Local infrastructure stack
├── Dockerfile            # Service containerization (prod-ready)
└── pom.xml               # Multi-module build
