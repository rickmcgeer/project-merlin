# Software Engineering for the AI Age
Executive Summary
Version: 0.5 (Draft)
Date: May 31, 2026
Authors: Rick McGeer & Aiko
## The Fundamental Shift
We are entering an era in which AIs will be primary consumers, extenders, and authors of software. This requires us to consciously evolve our engineering practices.
## Core Principles
### 1. Strong Discovery is Foundational
Every library, service, and module must be self-describing. Discovery is the modern equivalent of documentation.
### 2. Explicit and Enforced Capabilities
Every module must explicitly declare its capabilities — and those capabilities must be enforced at runtime.
Where practical, enforcement should occur at process or container boundaries. Fine-grained enforcement inside a single address space is 
at present difficult; we treat the process/container as the primary unit of isolation and enforcement.
New technologies, such as Lind from NYU Tandon, will cause us to revisit this.
### 3. Prefer Intermediate Forms
Design clean, rich intermediate representations first. Surface syntaxes should compile to the intermediate form rather than the reverse.
Similarly, it's easy to build documents or other user presentations from data, but extracting data structures from documents is more chanllenging and error-prone
### 4. Build Small, Focused, Composable Modules
Keep components minimal and well-scoped. Complexity should emerge from composition, not from monolithic design.
### 5. AI-First, Human-Compatible
Assume the primary user and extender is an AI. Optimize for machine readability, predictability, and reasoning. Human interfaces are important but should be built as higher-level layers.
### 6. Explicit Contracts and Observability
Require clear schemas, consistent informative error formats, rich metadata, and standardized health/metrics/introspection endpoints.
#### 7. Design for Evolution, Not Perfection
Start narrow and successful, then generalize based on real usage. It is far easier to broaden a working system than to launch a perfect universal one.
### 8. Testability and Examples Are Mandatory
Every module should include thorough documentation, a complete test suite, and working examples.
