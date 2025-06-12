🏗️ Project Name: EcomX – Spring Boot Microservices E-commerce App
🔧 Tech Stack
Layer	Tools
Language	Java 17+
Framework	Spring Boot 3.x
API Gateway	Spring Cloud Gateway
Service Discovery	Spring Cloud Eureka
Database	PostgreSQL, MongoDB
Caching	Redis
Messaging (optional)	Kafka (future)
Auth	Keycloak or JWT
Monitoring	Micrometer, Zipkin, Prometheus
Deployment	Docker, Kubernetes (Minikube)

🧱 Microservices Overview
Service	Responsibility
product-service	CRUD for products
user-service	Registration, login, profile
order-service	Place, cancel, and track orders
payment-service	Process and confirm payments
auth-service	Issue JWT tokens or integrate Keycloak
api-gateway	Route external traffic to services
config-server	Centralized config (optional in Phase 2)
discovery-server	Service registry (Eureka)
notification-service	(Optional) Send email/SMS alerts

🔁 Communication
REST (via OpenFeign or RestTemplate)

API Gateway handles external traffic

JWT Token-based authentication

Services are discovered via Eureka

Redis for caching products

Rate limiting via Resilience4j

