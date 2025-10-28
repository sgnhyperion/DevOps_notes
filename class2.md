## DevOps
DevOps is a set of practices and culture that combines **Development (Dev)** and **Operations (Ops)** to deliver software **faster and more reliably**.

---

## Key Ideas
- **DevOps Philosophy:** Dev and Ops work as one team.
- **Shift Left:** Testing and security are done early in development.

---

## Challenges
- Cultural change
- Resistance from teams using traditional processes

---

## Security Testing
- **SAST:** Scans source code without running it.
- **DAST:** Tests the running application.
- **SCA:** Finds vulnerabilities in third-party libraries.

**Example:**  
SQL Injection can be prevented using `PreparedStatement` instead of `Statement`.

---

## Continuous Integration (CI)
CI automatically:
- Fetches code
- Builds and tests it
- Runs security checks
- Creates deployable artifacts

* When we push code there should be a pipeline that should automatically:
    * Download code --> Linting --> Building --> Unit Testing(mocking and testing) --> SCA(Software Compliance Analysis) --> SAST(Static Analysis Security Testing) --> Dockerize(create Images) --> Testing --> Push Image into Artifact repository  
---

## Continuous Deployment (CD)
CD automatically deploys code after CI passes, with manual approval only if needed.

---

## Communication
- **API Gateway:** Routes requests and handles authentication.
- **Microservices:** Communicate synchronously or asynchronously (Kafka/RabbitMQ).

---

## Summary
DevOps improves **speed, collaboration, automation, and reliability** in software delivery.
