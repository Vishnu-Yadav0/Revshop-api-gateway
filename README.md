![API Gateway Banner](https://raw.githubusercontent.com/Vishnu-Yadav0/Revshop-api-gateway/main/banner.png)

# ⚙️ RevShop — API Gateway

Central entry point for the RevShop microservices platform. Handles all inbound traffic, routes requests to the appropriate service, enforces rate limiting, and wraps calls with Resilience4j circuit breakers.

[![Java](https://img.shields.io/badge/Java-17-orange?style=flat-square&logo=openjdk)](https://openjdk.org/)
[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.x-brightgreen?style=flat-square&logo=springboot)](https://spring.io/projects/spring-boot)
[![Spring Cloud](https://img.shields.io/badge/Spring%20Cloud-Gateway-blue?style=flat-square)](https://spring.io/projects/spring-cloud-gateway)
[![Docker](https://img.shields.io/badge/Docker-Containerized-blue?style=flat-square&logo=docker)](https://www.docker.com/)

---

## What it does

- Routes all client requests to the correct downstream microservice
- Enforces JWT validation before forwarding requests
- Rate-limits incoming traffic to protect services from overload
- Uses **Resilience4j** circuit breakers to handle downstream failures gracefully
- Integrates with **Eureka** for dynamic service resolution (no hardcoded URLs)

## Tech Stack

| Layer | Tech |
|---|---|
| Framework | Spring Boot 3, Spring Cloud Gateway |
| Fault Tolerance | Resilience4j Circuit Breaker |
| Auth | JWT validation |
| Service Discovery | Netflix Eureka Client |
| Config | Spring Cloud Config Client |
| Tracing | Zipkin, Micrometer |
| Container | Docker |

## Running Locally

> Make sure Eureka and Config Server are running first.

```bash
./mvnw spring-boot:run
```

Or with Docker:

```bash
docker build -t revshop-api-gateway .
docker run -p 8080:8080 revshop-api-gateway
```

## Default Port

`8080`

---

## Part of RevShop Microservices

| Service | Repo |
|---|---|
| 🌐 Frontend | [Revshop-frontend](https://github.com/Vishnu-Yadav0/Revshop-frontend) |
| ⚙️ API Gateway | [Revshop-api-gateway](https://github.com/Vishnu-Yadav0/Revshop-api-gateway) |
| 🔍 Service Discovery | [Revshop-service-discovery](https://github.com/Vishnu-Yadav0/Revshop-service-discovery) |
| 🗂️ Config Server | [Revshop-config-server](https://github.com/Vishnu-Yadav0/Revshop-config-server) |
| 👤 User Service | [Revshop-user-service](https://github.com/Vishnu-Yadav0/Revshop-user-service) |
| 🛍️ Product Catalog | [Revshop-product-catalog-service](https://github.com/Vishnu-Yadav0/Revshop-product-catalog-service) |
| 📦 Inventory | [Revshop-inventory-service](https://github.com/Vishnu-Yadav0/Revshop-inventory-service) |
| 🛒 Order/Sales | [Revshop-order-sales-service](https://github.com/Vishnu-Yadav0/Revshop-order-sales-service) |
| 💳 Payment | [Revshop-payment-service](https://github.com/Vishnu-Yadav0/Revshop-payment-service) |
| 🔔 Notification | [Revshop-notification-service](https://github.com/Vishnu-Yadav0/Revshop-notification-service) |
| 🚚 Shipping | [Revshop-shipping-service](https://github.com/Vishnu-Yadav0/Revshop-shipping-service) |
| 🤖 AI Chat | [Revshop-ai-chat-service](https://github.com/Vishnu-Yadav0/Revshop-ai-chat-service) |

