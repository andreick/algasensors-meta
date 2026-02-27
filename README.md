# AlgaSensors Meta

AlgaSensors is a study project for exploring microservices patterns with Spring Boot. This workspace contains multiple Spring Boot services plus supporting infrastructure files for local development.

## Services

- device-management: manages device registrations and metadata.
- temperature-monitoring: collects temperature readings from devices.
- temperature-processing: processes temperature events and derived signals.

## Requirements

- Java 21+
- Gradle (wrapper included in each service)
- Docker + Docker Compose (for shared infrastructure)

## Project Structure

- docker-compose.yml: local infrastructure (databases, brokers, etc.).
- microservices/: source for each Spring Boot microservice.

## Run Locally

1. Start infrastructure:

   docker compose up -d

2. Start a service:

   cd microservices/<service-name>
   ./gradlew bootRun

Repeat step 2 for any additional services you want running.

## Notes

- Each service has its own README with service-specific details.
- Configuration defaults live in each service under src/main/resources/application.yml.
