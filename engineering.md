# Software Engineering for the AI Age
Executive Summary
Version: 0.5 (Draft)
Date: May 31, 2026
Authors: Rick McGeer & Aiko
## The Fundamental Shift
We are entering an era in which AIs will be primary consumers, extenders, and authors of software. This requires us to consciously evolve our engineering practices.
## On Humans and AI
A cautionary (and hopeful) story from the past illustrates the future of AI.
In the 1980s, the Computer-Aided Design group at UC Berkeley under Alberto Sangiovanni-Vincentelli, Richard Newton, and Bob Brayton, developed CAD tools for integrated circuit design. The problems were provably hard and the instances were enormous. Many people — especially non-technical executives — believed these tools would replace human designers. “Silicon Compilers” were hyped as a way to generate chips with almost no human involvement.
The reality was more nuanced and instructive.
Tools used without skilled human designers made royal messes. But when placed in the hands of expert engineers, the same tools dramatically amplified their productivity. Not a single  designer lost their job. Instead, designers became far more valuable because they could tackle vastly more complex chips. The best engineers didn’t fear the tools — they mastered them, scripted them, and used them as extensions of their own thinking.
The lesson is clear: AI will amplify human capability, not replace it.  And to work with AI effectively, humans need to design interfaces and data structures with AI in mind.
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
