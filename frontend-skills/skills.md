name: frontend-sensible-defaults
description: This skill should be used when determining, configuring, or validating the frontend technical stack, languages, and frameworks for operational and transactional web applications within TechOps.
triggers:
- frontend defaults
- frontend programming language
- frontend framework
- SPA hosting
- PWA hosting
- ReactJS configuration
---

# Frontend Sensible Defaults

[cite_start]An overview of the recommended frontend technologies and frameworks tailored for Modern Web Apps (Single Page Applications / Progressive Web Apps) to drive consistency, enable micro-frontends, and eliminate delivery friction[cite: 6, 16, 144, 145].

## Core Instructions

When developing client-facing web applications or user interfaces, implement the following tech stack standards:

* [cite_start]**Primary Programming Language:** Use the latest version of **ECMAScript (JavaScript)** as the default choice[cite: 135]. [cite_start]Because target users primarily utilize up-to-date modern browsers, teams can comfortably push into newer language versions using compilers like Babel[cite: 136, 137].
* [cite_start]**Primary Framework:** Adopt **ReactJS** as the universal frontend framework[cite: 143]. [cite_start]Adhering to a single framework is necessary to successfully support micro-frontends in large applications and reduce cognitive overhead across teams[cite: 144, 145].
* [cite_start]**JS Compiler Restrictions:** Avoid utilizing alternative JavaScript compilers such as **CoffeeScript** or **ClojureScript**[cite: 140]. [cite_start]They introduce language proliferation into the ecosystem and add technical complexity with minimal productivity gains[cite: 140, 141].
* [cite_start]**Framework Guardrails:** Refrain from adopting alternative frameworks like **Angular** or **VueJS** in standard production environments, as they lack widespread institutional adoption across teams[cite: 150].

## Common Patterns

### 1. Standard Modern Web App (SPA / PWA)
* [cite_start]**Language:** Latest version of ECMAScript (JavaScript) compiled via Babel[cite: 135, 137].
* [cite_start]**Framework:** ReactJS[cite: 143].
* [cite_start]**Use Case:** Standard web portals, static asset setups, and applications seeking seamless alignment with internal support pipelines and quick security assurance reviews[cite: 16, 327].

### 2. Large-Scale or Enterprise Codebase (Acceptable Alternative)
For sophisticated frontend codebases that scale across multiple modules or require robust architecture management:
* [cite_start]**Language:** **TypeScript** is officially recommended as an acceptable alternative due to its interoperability with ECMAScript and high-quality static type support[cite: 135, 138, 139].
* [cite_start]**Framework:** ReactJS[cite: 143].

### 3. Lightweight Prototyping & Shared Hosting (Under Evaluation)
When looking to spin up quick application prototypes or leverage serverless backend suites:
* [cite_start]**Platforms:** Technologies like **Google Firebase** and **Amazon Amplify** offer streamlined database syncing, authentication, and hosting tools[cite: 153, 154, 156, 158]. 
* [cite_start]**Guideline:** Because widespread organizational adoption is not yet established, these tools should currently be categorized under **responsible experimentation** rather than a core default[cite: 160, 161].

## Additional Resources

* `TechOps TechStack Sensible Defaults - 2023 Edition.pdf` — Section: "Frontend" (Pages 4, 13–15).