# Roboshop Application - Payment Microservice CICD

This repository contains the **Payment** microservice for the **Roboshop Application**, a microservices-based e-commerce platform for selling robots. The Payment service is responsible for handling payment processing and integration within the Roboshop ecosystem.

---

## Table of Contents

- [Overview](#overview)
- [Key Features](#key-features)
- [Tech Stack](#tech-stack)
- [CI/CD Pipeline](#cicd-pipeline)
- [Deployment](#deployment)
- [Getting Started](#getting-started)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

---

## Overview

**Roboshop** is a cloud-native, microservices-driven e-commerce platform. Each functionality (cart, payment, user, etc.) is isolated into its own service. This repository provides the Payment microservice, which manages payment workflows, integrations, and transaction records.

---

## Key Features

- Handles payment processing for the Roboshop platform
- Integrates with payment gateways (customize as per your requirements)
- RESTful APIs for payment operations
- Built for cloud-native deployment (containerized, stateless)
- Automated CI/CD with Jenkins and EKS

---

## Tech Stack

- **Language:** Python
- **Framework:** (e.g., Express, Flask, Spring Boot)
- **Containerization:** Docker
- **CI/CD:** Jenkins, [Jenkins Shared Library](https://github.com/subbu20n/jenkins-shared-library)
- **Orchestration:** Kubernetes (EKS)
- **Cloud:** AWS

---

## CI/CD Pipeline

- Automated build and deployment using Jenkins
- Uses a centralized Jenkins Shared Library for pipeline best practices and code reuse
- Docker images are built and pushed to the configured registry
- Deployed to Amazon EKS for scalability and high availability

### Jenkinsfile

This repository contains a `Jenkinsfile` which defines the CI/CD pipeline stages. The shared library handles common pipeline logic for consistency and maintainability.

---

## Deployment

The Payment service is designed for cloud deployment on Kubernetes (EKS).

**Deployment Steps:**
1. Clone the repository and configure environment variables.
2. Build the Docker image:
   ```bash
   docker build -t <your-repo>/payment:<tag> .
   ```
3. Push the image to your registry:
   ```bash
   docker push <your-repo>/payment:<tag>
   ```
4. Deploy to EKS using your preferred Kubernetes manifests or Helm charts.

> **Note:** The Jenkins pipeline automates these steps as part of CI/CD.

---

## Getting Started

```bash
# Clone the repo
git clone https://github.com/subbu20n/payment.git
cd payment

# (Optional) Set up your local development environment
# (Instructions depend on your language/runtime)

# Run locally (example for Node.js)
npm install
npm start
```

---

## Project Structure

```
payment/
├── src/               # Source code for the payment service
├── Jenkinsfile        # Jenkins pipeline definition
├── Dockerfile         # Docker build instructions
├── README.md          # Project documentation
└── ...                # Other supporting files and configs
```

---

## Contributing

Contributions are welcome. Please open issues or submit pull requests for improvements and fixes. Refer to the [CONTRIBUTING.md](CONTRIBUTING.md) (if available) for more details.

---

## License

This project is licensed under the [MIT License](LICENSE).