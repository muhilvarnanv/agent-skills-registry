name: backend-sensible-defaults
description: This skill should be used when determining or validating the backend technical stack, programming languages, frameworks, or database choices for operational and transactional systems within TechOps.
triggers:
- backend defaults
- backend programming language
- backend framework
- database choice
- relational database
- nosql data store
---

# Backend Sensible Defaults

[cite_start]An overview of the recommended backend technologies, frameworks, and data stores tailored for Operational (Transactional) Systems to maximize consistency, reduce team friction, and streamline maintenance[cite: 30, 132].

## Core Instructions

[cite_start]When designing, updating, or auditing backend services, adhere to the following architectural guidelines[cite: 127]:

* [cite_start]**Primary Programming Language:** Use **Python** as the default language for building modern applications and services[cite: 164, 167]. [cite_start]Stick to Python and its associated tooling unless a specific differentiator requires a deviation[cite: 168].
* [cite_start]**Primary Framework:** Use **Flask** when building on the Python stack[cite: 185]. [cite_start]Teams must restrict themselves to one primary backend framework per application, and introduce no more than two backend frameworks overall to keep the stack manageable[cite: 191, 193].
* [cite_start]**Relational Database Management System (RDBMS):** Select **PostgreSQL** as the default relational database[cite: 199, 203]. 
* [cite_start]**NoSQL Data Store:** Select **Firestore** (in GCP) when your business challenges strictly necessitate modeling and storing data in document structures[cite: 214, 215].
* [cite_start]**Hosting Architecture:** Default to **Serverless Technologies** (e.g., Google Cloud Functions, Express/Flask on Cloud Run) for optimal hosting[cite: 249, 255]. [cite_start]Lightweight frameworks or no frameworks should be favored when constrained by serverless CPU/memory environments[cite: 195, 196]. 
* [cite_start]**Container/VM Guardrails:** Avoid Kubernetes (K8s) and Virtual Machines (VMs) unless the application explicitly demands massive computational scale or unique infrastructure optimization[cite: 260, 261].

## Common Patterns

### 1. Standard Enterprise Microservice
* [cite_start]**Language:** Python [cite: 164]
* [cite_start]**Framework:** Flask [cite: 185]
* [cite_start]**Database:** PostgreSQL (Fully managed via GCP Cloud SQL or AWS RDS) [cite: 199, 200]
* [cite_start]**Hosting:** Google Cloud Run or AWS Lambda [cite: 236, 255]

### 2. Event-Driven or High-Productivity JVM Stack (Acceptable Alternative)
[cite_start]When specialized infrastructure is required (such as better tool integration with Kafka) or when team skill constraints prevent a quick ramp-up to Python, teams may leverage the JVM Stack[cite: 170, 171, 173]:
* [cite_start]**Language:** **Kotlin** (strongly preferred over Java due to productivity gains and modern language features)[cite: 165, 174, 175].
* [cite_start]**Framework:** **Spring**[cite: 186].

### 3. Full-Stack JavaScript/TypeScript Unified Eco-system (Acceptable Alternative)
[cite_start]For teams looking to share code or maintain high developer productivity by utilizing the same language platform across both frontend and backend domains[cite: 180]:
* [cite_start]**Language:** Latest version of **ECMAScript** or **TypeScript** (preferred for larger codebases due to type safety)[cite: 178, 179].
* [cite_start]**Runtime:** **NodeJS** (the sensible runtime default choice over Deno due to widespread institutional knowledge)[cite: 181, 183].
* [cite_start]**Framework:** **ExpressJS**[cite: 186].

### 4. Alternative Relational Choice (Acceptable Alternative)
* [cite_start]**Database:** **MySQL** is officially recognized as an acceptable relational alternative if specific project constraints or legacy team expertise heavily dictate its use over PostgreSQL[cite: 204, 207].

## Additional Resources

* [cite_start]`TechOps TechStack Sensible Defaults - 2023 Edition.pdf` — Section: "The Recommended Tech Stack for Operational Systems (Transactional Systems)" (Pages 4, 14–17)[cite: 6, 10].