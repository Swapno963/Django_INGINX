# Django Microservices with Nginx Reverse Proxy

This project demonstrates a Django-based microservices architecture, using Nginx as a reverse proxy, load balancer, SSL terminator, and caching layer. With Nginx, this setup achieves enhanced performance, security, and scalability for Django microservices.

## Features

- **Reverse Proxy**: Nginx routes client requests to specific Django services based on endpoint paths, enabling multiple services to be accessed via a single endpoint.
- **Load Balancing**: Distributes incoming traffic across multiple instances of each Django service, preventing overload on any single instance.
- **SSL Termination**: Handles SSL/TLS encryption, reducing the computational load on Django services.
- **Caching**: Caches static files and frequently requested HTTP responses, reducing load and improving response times.
- **Rate Limiting & Security**: Provides rate limiting and request validation to help prevent abuse and DoS attacks.
- **Service Discovery & Routing**: Routes requests based on service availability in dynamic microservice setups, allowing seamless interaction with scaling services.

## Project Structure

The project structure includes multiple Django services, with Nginx managing request distribution:

```plaintext
project-root/
├── service1/                # Django Service 1
├── service2/                # Django Service 2
├── nginx/
│   ├── conf.d/
│   │   └── default.conf     # Nginx configuration for reverse proxy, load balancing, etc.
│   └── Dockerfile           # Dockerfile for Nginx
├── docker-compose.yml       # Docker Compose file to orchestrate services
└── README.md                # Project documentation
```
