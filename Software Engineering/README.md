# Software Engineering

Created: August 11, 2026 10:26 AM
Status: Not started

- Unit 1
    
    [Introduction To Software Engineering ](Introduction%20To%20Software%20Engineering.md)
    
    [Explained](Explained.md)
    
- Unit 2
    
    [Unit 2-Agile Soft Development](Unit%202-Agile%20Soft%20Development.md)
    
    [Case-Study-Agile-SDLC](Case-Study-Agile-SDLC.md)
    
- Mid Sem Imp Ques
    
    ### Q1. What is Software Engineering?
    
    **Definition (IEEE):** Software Engineering is the application of a systematic, disciplined, and quantifiable approach to the development, operation, and maintenance of software.
    
    - **Software** = a program or set of programs with instructions that provide functionality.
    - **Engineering** = designing and building something that serves a purpose efficiently and cost-effectively.
    - So Software Engineering = an engineering discipline applied to building software — not just writing code, but planning, designing, testing, and maintaining it properly.
    
    **Key points to write:**
    
    - It is the systematic process of designing, developing, testing, and maintaining software using requirements analysis, design, testing, and maintenance techniques.
    - It ensures software is high-quality, reliable, and maintainable — especially important for large systems.
    - It improves efficiency, quality, and budget management, helping deliver software on time, within budget, and meeting all requirements.
    - It continuously adopts new tools and methodologies to handle complexity and evolving technology.
    
    **Dual Role of Software** (add this for extra marks):
    
    1. **As a Product** — delivers computing potential across hardware networks; acts as an information transformer (produces, manages, modifies, transmits information).
    2. **As a Vehicle for Delivering a Product** — provides system functionality (e.g. payroll system), controls other software (e.g. an OS), or helps build other software (e.g. software tools).
    
    ---
    
    ### Q2. What are its Core Principles and Goals?
    
    **Goals of Software Engineering:**
    
    1. Develop high-quality software.
    2. Complete the project within time and budget.
    3. Produce reliable and efficient software.
    4. Make software easy to maintain and upgrade.
    5. Meet customer requirements.
    6. Reduce development cost and risks.
    
    **Core Principles of Software Engineering:**
    
    1. **Modularity** — divide software into small, independent parts that are easy to develop and test.
    2. **Abstraction** — show only what is necessary; hide internal implementation details.
    3. **Encapsulation** — keep data and related functions together, protected from outside access.
    4. **Maintenance** — regularly update software to fix bugs, improve features, enhance security.
    5. **Testing** — check the software works correctly and meets requirements.
    6. **Design Patterns** — use proven, reusable solutions to common design problems.
    7. **Agile Methodologies** — develop in small steps with frequent feedback and flexibility.
    8. **Continuous Integration & Deployment (CI/CD)** — frequently merge code changes and automatically deploy updates.
    
    *Bonus if you have space* — **Characteristics of Good Software**: Correctness, Reliability, Efficiency, Usability, Maintainability, Portability, Security.
    
    ---
    
    ### Q3. Waterfall Model — its different phases
    
    **Definition:** A traditional, **linear, sequential** SDLC model where each phase must be fully completed before the next one begins.
    
    **Diagram:**
    
    ```
    Requirements → Design → Development → Testing → Deployment → Maintenance
    ```
    
    **Phases explained in detail:**
    
    1. **Requirements Analysis & Specification** — gather and analyse customer needs; document as the SRS (Software Requirement Specification), a formal agreement between customer and developer.
    2. **Design** — HLD (overall architecture, major components, interactions) + LLD (detailed component logic and data flow); documented in the Software Design Document (SDD).
    3. **Development (Coding)** — developers write source code based on the design; unit testing performed on each module.
    4. **Testing & Deployment** — integration testing → system testing → Alpha testing (by dev team) → Beta testing (by selected users) → Acceptance testing (by customer) → deployment (environment setup, user training, final checks).
    5. **Maintenance** — Corrective (fix errors), Perfective (enhance features), Adaptive (adapt to new environments), Preventive (prevent future issues).
    
    **When to use it:** stable/well-documented requirements, minimal expected changes, small-to-medium projects, strict regulatory compliance, client prefers step-by-step process.
    
    **Advantages:** easy to understand, clear milestones, strong documentation, disciplined process, good for stable-requirement projects.
    
    **Disadvantages:** hard to accommodate change once a phase is done, customer only sees the software at the very end, risky if requirements were misunderstood early.
    
    **Example — Online Food Delivery System:** Analysis (registration, menu, payment features) → Design (architecture, DB, UI, payment gateway) → Development (login, search, order, payment modules) → Testing (order/payment/tracking checks) → Maintenance (bug fixes, new restaurants, security updates).
    
    ---
    
    ### Q4. V-Model
    
    **Definition:** The V-Model integrates **testing and validation at every stage** of development. It follows a "V" shape — each development phase on the left is directly mapped to a corresponding testing phase on the right, so defects are caught early.
    
    **Diagram:**
    
    ```
    Requirement Analysis  <--Acceptance Test Design-->  Acceptance Testing
         System Design     <--System Test Design-->      System Testing
              Architecture Design <--Integration Test Design--> Integration Testing
                   Module Design  <--Unit Test Design-->  Unit Testing
                             \                    /
                                  Coding
    ```
    
    (Left arm goes DOWN = Verification; bottom point = Coding; right arm goes UP = Validation.)
    
    **1. Verification Phases (left arm — static, done WITHOUT running code):**
    
    - Business Requirement Analysis → prepare Acceptance Test Plans
    - System Design → plan System Testing
    - Architectural Design → prepare Integration Test Cases
    - Module Design (LLD) → prepare Unit Test Cases
    - Coding → bottom of the V
    
    **2. Validation Phases (right arm — dynamic, done BY EXECUTING code):**
    
    - Unit Testing → eliminate bugs at unit level
    - Integration Testing → modules integrated and tested together
    - System Testing → whole application tested together
    - User Acceptance Testing (UAT) → in a production-like environment
    
    **Principles:** Large to Small, Data/Process Integrity, Scalability, Cross Referencing (each requirement maps to a test).
    
    **Applications:** Healthcare systems, Banking/financial software, Aerospace & aviation, Automotive (ABS, airbags, ADAS).
    
    **Advantages:** disciplined phase-by-phase process, early defect detection, strong testing focus.
    
    **Disadvantages:** can't handle changing requirements well, time-consuming (heavy documentation/testing), no iterative development, not for complex/high-risk projects.
    
    ---
    
    ### Q5. Requirement Elicitation and Analysis
    
    #### Requirement Elicitation
    
    **Definition:** The process of gathering information from stakeholders to understand what they need from the software system. It is the **first step** in Requirement Engineering.
    
    **Objectives:** understand customer needs, identify system features, resolve misunderstandings, collect complete and correct requirements.
    
    **Process:**
    
    ```
    Identify Stakeholders → Gather Requirements → Analyze Requirements → Validate Requirements → Document Requirements
    ```
    
    **Techniques:**
    
    | Technique | Description |
    | --- | --- |
    | Interview | Direct discussion with customers/users |
    | Questionnaire | Collect information using forms |
    | Observation | Observe users while working |
    | Brainstorming | Group discussion to generate ideas |
    | Workshops | Meetings involving all stakeholders |
    | Prototyping | Build a sample system for feedback |
    | Document Analysis | Study existing documents/systems |
    
    **Advantages:** better understanding of customer expectations, reduces project risk, improves quality, prevents costly changes later.
    
    #### Requirement Analysis
    
    **Definition:** The process of examining, organizing, validating, and prioritizing the gathered requirements.
    
    **Activities:** classify requirements, detect conflicts, remove ambiguities, prioritize requirements, check feasibility, validate with stakeholders.
    
    **Process:**
    
    ```
    Collected Requirements → Classification → Conflict Resolution → Prioritization → Validation → Final Requirements
    ```
    
    **Importance:** eliminates errors early, improves customer satisfaction, helps accurate estimation, reduces development cost.
    
    ---
    
    ### Q6. Different Types of Software Requirements
    
    **IEEE 729 definition of a requirement:** a condition/capability needed by a user to solve a problem or achieve an objective; OR a condition/capability a system must meet to satisfy a contract/standard/specification; OR a documented representation of either.
    
    **Three types:**
    
    1. **Functional Requirements** — define **WHAT** the system should do (features/operations). Specific, measurable, testable. *Examples:* user login, registration, search products, add to cart, generate reports, print invoice.
    2. **Non-Functional Requirements** — define **HOW** the system should perform (quality/constraints). *Examples:* performance, security, reliability, availability, maintainability, scalability, usability.
    3. **Domain Requirements** — requirements that arise from the specific application domain/industry the software serves.
    
    **Example (Online Banking System):**
    
    - *Functional:* log in with username/password; check account balance; receive transaction notifications.
    - *Non-functional:* respond within 2 seconds; encrypted transactions; handle 100 million users with minimal downtime.
    
    **Quick comparison:**
    
    | Functional | Non-Functional |
    | --- | --- |
    | What the system does | How the system performs |
    | Feature-based, user-visible | Quality-based, mostly system-level |
    | Easy to test | Harder to measure |
    
    ---
    
    ### Q7. SDLC — and difference between HLD and LLD
    
    #### Part A: SDLC
    
    **Definition:** SDLC is a structured process used to plan, design, develop, test, deploy, and maintain software, aligning development with business goals and user requirements.
    
    **6 Phases:**
    
    ```
    Requirement Analysis → System Design → Implementation → Testing → Deployment → Maintenance
    ```
    
    1. **Requirement Analysis** — collect requirements, study feasibility, prepare SRS.
    2. **System Design** — design architecture, database, UI.
    3. **Implementation (Coding)** — write code following standards.
    4. **Testing** — detect and remove bugs.
    5. **Deployment** — install at customer site, train users.
    6. **Maintenance** — correct errors, improve performance, add features.
    
    **Benefits:** organised framework for managing phases, early defect detection (lower cost/time), ensures high-quality delivery meeting user expectations.
    
    #### Part B: HLD vs LLD
    
    System Design (SDLC's 3rd phase) itself splits into two levels:
    
    | High-Level Design (HLD) | Low-Level Design (LLD) |
    | --- | --- |
    | Defines the overall system architecture | Focuses on detailed component-level design |
    | Describes modules and their interactions | Describes internal logic of each module |
    | Also called macro-level / system design | Also called micro-level / detailed design |
    | Created by solution architects | Created by developers/designers |
    | Based on the SRS | Based on the reviewed HLD |