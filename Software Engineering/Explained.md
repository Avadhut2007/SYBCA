# Explained

# UNIT 1: INTRODUCTION TO SOFTWARE ENGINEERING AND SOFTWARE PROCESS

==================================================

### DEFINITION AND GOALS OF SOFTWARE ENGINEERING

DEFINITION

Software Engineering is a systematic, disciplined, and quantifiable approach to the design, development, operation, and maintenance of software. It applies engineering principles to software creation so that the resulting product is reliable, efficient, and works on real machines.

IEEE Definition: “The application of a systematic, disciplined, quantifiable approach to the development, operation, and maintenance of software; that is, the application of engineering to software.”

#### WHY SOFTWARE ENGINEERING IS NEEDED

- Software is complex, intangible, and constantly evolving.
- Large projects fail without structured processes (missed deadlines, budget overruns, poor quality).
- “Software crisis” of the 1960s–70s (projects late, over budget, unreliable, hard to maintain) motivated formal engineering practices.

GOALS OF SOFTWARE ENGINEERING

1. Maintainability – Software should be easy to modify/extend as requirements change.
2. Efficiency – Optimal use of resources (memory, processing time, storage).
3. Reliability – Software should perform its intended functions consistently without failure.
4. Reusability – Modules/components should be reusable in other projects.
5. Portability – Software should run on different platforms/environments with minimal changes.
6. Cost-effectiveness – Development within budget without compromising quality.
7. Timeliness – Delivered within the scheduled time frame.
8. Scalability – Ability to handle growth in users/data/functionality.
9. User Satisfaction – Meeting user needs and expectations (usability, correctness).
10. Quality – Conforms to specified requirements and standards.

SOFTWARE ENGINEERING VS PROGRAMMING

Programming: Focus on writing code
Software Engineering: Focus on entire lifecycle (analysis, design, testing, maintenance)

Programming: Individual activity
Software Engineering: Team-based, process-driven activity

Programming: No formal documentation needed
Software Engineering: Requires documentation, standards, and process discipline

Programming: Small-scale problem solving
Software Engineering: Large-scale, complex system building

==================================================

### SOFTWARE DEVELOPMENT LIFE CYCLE (SDLC) MODELS

The SDLC is a structured sequence of phases followed to develop software: Requirement Analysis → Design → Implementation → Testing → Deployment → Maintenance.

#### 2.1 WATERFALL MODEL

- Linear, sequential model — each phase must complete before the next begins.
- Phases: Requirements → Design → Implementation → Verification → Maintenance.
- Advantages: Simple, easy to understand and manage; well-documented; works well for small, well-understood projects.
- Disadvantages: No feedback loop; inflexible to changes; working software available only late in the cycle; risky for large/complex projects.

#### 2.2 INCREMENTAL MODEL

- Requirements are divided into builds/increments; each increment adds functionality.
- Combines elements of waterfall applied repeatedly.
- Advantages: Working software produced early; easier to test and debug smaller increments; customer feedback incorporated between increments.
- Disadvantages: Requires good planning and design; total cost may be higher than waterfall.

#### 2.3 RAD (RAPID APPLICATION DEVELOPMENT) MODEL

- Emphasizes rapid prototyping and quick feedback with minimal planning.
- Uses component-based construction and heavy user involvement.
- Advantages: Fast development; reduced development time; encourages customer feedback.
- Disadvantages: Requires skilled developers; not suitable for large, complex, or high-risk projects; needs modularization capability.

#### 2.4 SPIRAL MODEL

- Combines iterative development with systematic risk analysis.
- Each cycle (spiral) involves: Planning → Risk Analysis → Engineering → Evaluation.
- Advantages: Strong risk management; suitable for large, complex, high-risk projects; incorporates customer feedback at every loop.
- Disadvantages: Costly; requires risk-assessment expertise; complex to manage.

#### 2.5 V-MODEL (VERIFICATION AND VALIDATION)

- Extension of waterfall; each development phase has a corresponding testing phase forming a “V” shape.
- Requirements ↔︎ Acceptance Testing, Design ↔︎ System Testing, Module Design ↔︎ Unit Testing.
- Advantages: Testing planned early; higher chance of success; disciplined.
- Disadvantages: Rigid like waterfall; no working software until late; not suited for changing requirements.

#### 2.6 AGILE MODEL

- Iterative and incremental approach emphasizing flexibility, collaboration, and customer feedback.
- Development happens in short cycles called sprints (typically 2–4 weeks).
- Based on the Agile Manifesto values: individuals & interactions over processes & tools; working software over comprehensive documentation; customer collaboration over contract negotiation; responding to change over following a plan.
- Popular frameworks: Scrum, XP (Extreme Programming), Kanban.
- Advantages: Handles changing requirements well; frequent delivery of working software; continuous customer involvement.
- Disadvantages: Less predictable in cost/time; requires experienced teams; documentation may be minimal.

#### 2.7 PROTOTYPE MODEL

- A working prototype (mock-up) of the system is built first to gather clearer requirements before actual development.
- Advantages: Helps clarify unclear requirements; reduces risk of building the wrong product.
- Disadvantages: Users may mistake prototype for final product; can increase development time/cost if overused.

==================================================

### ROLES AND RESPONSIBILITIES IN SOFTWARE DEVELOPMENT TEAMS

Role: Project Manager
Responsibilities: Planning, scheduling, budgeting, resource allocation, risk management, coordinating between client and team

Role: Business Analyst
Responsibilities: Gathering and analyzing requirements, bridging communication between client and technical team

Role: Software Architect
Responsibilities: Designing overall system architecture, choosing technologies, ensuring scalability and maintainability

Role: Software Developer/Programmer
Responsibilities: Writing, debugging, and implementing code according to design specifications

Role: Software Designer
Responsibilities: Creating detailed design (UML diagrams, data flow, module structure) from requirements

Role: Quality Assurance (QA)/Tester
Responsibilities: Designing test cases, executing tests, verifying software meets requirements, identifying defects

Role: UI/UX Designer
Responsibilities: Designing user interfaces and ensuring good user experience

Role: DevOps Engineer
Responsibilities: Managing deployment pipelines, CI/CD, infrastructure, monitoring

Role: Database Administrator (DBA)
Responsibilities: Designing, implementing, and maintaining databases

Role: Technical Writer
Responsibilities: Preparing documentation (user manuals, technical specs)

Role: Client/Stakeholder
Responsibilities: Providing requirements, feedback, and final acceptance of the product

Role: Scrum Master (Agile teams)
Responsibilities: Facilitating Agile ceremonies, removing team blockers, ensuring process adherence

Role: Product Owner (Agile teams)
Responsibilities: Managing product backlog, prioritizing features, representing customer interests

Key point: Clear role definition avoids duplication of effort, ensures accountability, and improves communication and efficiency within the team.

==================================================

### ETHICAL AND PROFESSIONAL ISSUES IN SOFTWARE ENGINEERING

WHY ETHICS MATTER

Software engineers build systems that affect people’s lives, safety, privacy, and finances (e.g., medical software, banking systems, autonomous vehicles), so ethical responsibility is critical.

ACM/IEEE CODE OF ETHICS – KEY PRINCIPLES

1. Public Interest – Act consistently with public interest and safety.
2. Client and Employer – Act in the best interests of client/employer, consistent with public interest.
3. Product – Ensure products/modifications meet the highest professional standards.
4. Judgment – Maintain integrity and independence in professional judgment.
5. Management – Managers/leaders should follow ethical approaches to software development and management.
6. Profession – Advance the integrity and reputation of the profession.
7. Colleagues – Be fair to and supportive of colleagues.
8. Self – Participate in lifelong learning and promote ethical practice.

COMMON ETHICAL/PROFESSIONAL ISSUES

- Confidentiality – Protecting client/user data and proprietary information.
- Intellectual Property Rights – Respecting copyrights, patents, software licenses; avoiding plagiarism/piracy.
- Privacy – Ensuring user data is collected, stored, and used responsibly (e.g., GDPR compliance).
- Competence – Not undertaking work beyond one’s expertise; maintaining skill currency.
- Honesty – Not misrepresenting capabilities, timelines, or product quality to clients/employers.
- Software Piracy – Illegal copying/distribution of software.
- Liability – Responsibility for software defects that cause harm (e.g., safety-critical systems).
- Whistleblowing – Reporting unethical practices even at personal/professional risk.
- Conflict of Interest – Avoiding situations where personal interest conflicts with professional duty.
- Accessibility – Designing software usable by people with disabilities.
- Bias and Fairness – Avoiding discriminatory outcomes in algorithms (especially AI/ML systems).

==================================================

1. SOFTWARE PROCESSES

A software process is a set of related activities that leads to the production of a software product. It defines who does what, when, and how to reach a goal.

#### 5.1 SOFTWARE PROCESS MODELS

A structured framework describing how the process activities are organized. Common models:
- Waterfall Model
- Incremental Development Model
- Spiral Model
- Agile Process Models (Scrum, XP)

(These are detailed above under SDLC models — the same models represent both the lifecycle and the underlying process framework.)

#### 5.2 PROCESS ACTIVITIES (FUNDAMENTAL SOFTWARE ENGINEERING ACTIVITIES)

1. Software Specification (Requirements Engineering)
    - Defining what the system should do and the constraints on its operation.
    - Sub-activities: Feasibility study, Requirements elicitation & analysis, Requirements specification, Requirements validation.
2. Software Design and Implementation
    - Converting the specification into an executable system.
    - Sub-activities: Architectural design, Interface design, Component design, Database design, Coding/Programming.
3. Software Validation (Verification and Validation - V&V)
    - Checking the system conforms to its specification and meets customer needs.
    - Sub-activities: Unit testing, Integration testing, System testing, Acceptance testing.
    - Verification: “Are we building the product right?”
    - Validation: “Are we building the right product?”
4. Software Evolution (Maintenance)
    - Modifying the software after delivery to correct faults, improve performance, or adapt to a changed environment.
    - Types: Corrective (fixing bugs), Adaptive (adapting to new environment), Perfective (enhancing features/performance), Preventive (improving maintainability).

#### 5.3 COPING WITH CHANGE

Software requirements and environments change constantly, so processes must accommodate change efficiently. Two key approaches:

1. Change Avoidance
    - The process includes activities that anticipate possible changes before significant work is invested (e.g., prototyping, requirements validation) to prevent late rework.
2. Change Tolerance
    - The process is designed to allow changes to be incorporated efficiently even late in the lifecycle.
    - Achieved through:
        - Incremental Development – Deliver in small increments so changes only affect future increments.
        - System Prototyping – Build prototypes to expose problems in requirements early.
        - Version/Configuration Management – Tracking versions of software components (using tools like Git/SVN) so changes are managed systematically.
        - Agile Methods – Iterative cycles readily absorb evolving requirements.

Techniques to handle change:
- Requirements management and traceability.
- Regular customer feedback and iterative delivery.
- Modular/loosely coupled design to localize the impact of changes.
- Configuration management to track and control changes.

#### 5.4 PROCESS IMPROVEMENT

The activity of enhancing an existing software process to improve product quality, reduce costs, or shorten development time.

Why process improvement is needed:
- To reduce delivery time.
- To reduce overall project costs.
- To improve the quality of the software product.

General Process Improvement Cycle:
1. Process Measurement – Measure attributes of the current process/product (e.g., defect rates, time taken).
2. Process Analysis – Identify weaknesses, bottlenecks, and areas for improvement.
3. Process Change – Introduce changes/improvements based on analysis.

This cycle repeats continuously (Continuous Process Improvement – CPI).

Popular Process Improvement Frameworks/Models:

Model: CMM / CMMI (Capability Maturity Model Integration)
Description: Defines 5 maturity levels: Initial, Managed, Defined, Quantitatively Managed, Optimizing. Organizations improve process maturity to increase predictability and quality.

Model: ISO 9001
Description: International quality management standard applicable to organizations including software development.

Model: Six Sigma
Description: Data-driven approach to eliminate defects and reduce process variation.

Model: SPICE (ISO/IEC 15504)
Description: Framework for assessing software process capability.

Benefits of Process Improvement:
- Higher-quality software with fewer defects.
- More predictable schedules and budgets.
- Improved customer satisfaction.
- Better team productivity and morale.

==================================================

QUICK REVISION SUMMARY

- Software Engineering = engineering discipline applied to software; goals include reliability, maintainability, efficiency, portability, and cost-effectiveness.
- SDLC Models: Waterfall, Incremental, RAD, Spiral, V-Model, Agile, Prototype — each suited to different project types/risk levels.
- Team Roles: PM, BA, Architect, Developer, Tester, Designer, DBA, DevOps, etc. — each with distinct responsibilities.
- Ethics: Guided by ACM/IEEE Code of Ethics; covers confidentiality, IP rights, privacy, honesty, liability.
- Software Process = structured set of activities: Specification → Design & Implementation → Validation → Evolution.
- Coping with Change: via change avoidance (prototyping) and change tolerance (incremental development, version control).
- Process Improvement: Measure → Analyze → Change cycle; frameworks like CMMI, ISO 9001, Six Sigma.