# Software Development Lifecycle (SDLC) -
- The Software Development Life Cycle (SDLC) is a structured process used by software developers and organizations to design, develop, test, and deploy software applications efficiently and systematically.
- It outlines the steps necessary to produce high-quality software that meets customer expectations, is delivered on time, and is cost-effective.


![17352691386366562319715910957078](https://github.com/user-attachments/assets/a02e4add-36df-49f8-9d3c-21e13a271912)


- 1. Requirement Analysis -
  - Gather and analyze the requirements from stakeholders.
  - Define the project's scope, objectives, and deliverables.

- 2. Planning -
  - Develop a project plan, including timelines, resources, and budgets.
  - Identify potential risks and mitigation strategies.

- 3. System Design -
  - Define the architecture, components, interfaces, and data flows.
  - Create detailed design documents to guide developers.

- 4. Development -
  - Write and build the actual code based on design documents.
  - Use programming languages, frameworks, and tools suited for the project.

- 5. Testing -
  - Verify that the software meets the requirements and is free of defects.
  - Perform unit testing, integration testing, system testing, and user acceptance testing.

- 6. Deployment -
  - Release the software to the production environment.
  - Ensure proper configuration and monitor for any deployment issues

- 7. Maintenance -
  - Provide ongoing support, fix bugs, and update the software as needed.
  - Monitor performance and adapt to changing requirements or environments.



# SDLC Model -
# 1.Waterfall Model -
- The Waterfall Model is one of the earliest and most straightforward Software Development Life Cycle (SDLC) models.
- It follows a linear and sequential approach, where each phase must be completed before the next phase begins.
- There is no overlapping of phases.

### Disadvantages -
- Inflexible: Difficult to make changes once a phase is completed.
- Late Testing: Errors are found only after the coding phase.
- Not Suitable for Changing Requirements: Cannot adapt to evolving client needs.
- Delayed Feedback: The final product is delivered late, so users see results only at the end.
- High Risk: Mistakes in early stages are costly to fix.

# 2.Incremental Model -
- The Incremental Model is an SDLC approach where the software is developed and delivered in small, manageable pieces or increments.
- Each increment adds new functionality to the system, allowing partial working versions of the product to be released earlier.
- This approach is iterative and enables feedback at every stage.

### Disadvantages -
- Requires detailed planning for smooth integration.
- Dependency issues can cause delays.
- High initial cost for setting up architecture.
- Not suitable for small projects due to overhead.
- Testing complexity increases as increments are added.


# 3.Spiral Model -
- The Spiral Model is an SDLC model that combines iterative development with risk management.
- It is suitable for complex and high-risk projects, as it emphasizes identifying and mitigating risks at every stage of the development process.
- The model is represented as a spiral with several loops.
- Each loop corresponds to a development phase, and the project grows progressively.

### Disadvantages -
- Complex: Difficult to manage and requires detailed risk analysis.
- High Cost: Expensive due to frequent iterations and risk management.
- Time-Consuming: Repeated cycles can extend project timelines.
- Requires Skilled Management: Needs experienced project managers.
- Not Suitable for Small Projects: Inefficient for simple projects.

# 4.V-Model (Verification and Validation) -
- The V-Model (Verification and Validation model) is an SDLC model that emphasizes testing at every stage of development.
- It is an extension of the Waterfall Model, with a strong focus on quality by mapping each development phase to a corresponding testing phase.
- Verification Phases (Development Side):
    - These ensure that the product is designed correctly.
- Validation Phases (Testing Side):
    - These ensure that the product meets the requirements.


![17358824662073537571698305704387](https://github.com/user-attachments/assets/ef0e4d28-a532-455f-9552-8b09c31201c8)




### Disadvantages -
- Inflexible: Hard to make changes once a phase is completed.
- Late Testing: Testing is done after development, delaying defect discovery.
- Not Suitable for Changing Requirements: Difficult to adapt to evolving needs.
- High Cost: Extensive planning and documentation increase costs.
- Risk of Misunderstanding: Early mistakes in requirements can affect the entire process.


# 5.Agile Model -
- The Agile Model is a flexible way to develop software by working in small steps called iterations or sprints.
- It focuses on delivering parts of the software quickly, improving based on feedback, and adjusting to changes as the project progresses.

![17358826579823700077303983721965](https://github.com/user-attachments/assets/3801acba-c229-4014-b893-ce82caad3c5e)


##### How Agile Works -
- Divide the Work: Break the entire project into smaller tasks or pieces called "increments."
- Plan a Sprint: A sprint is a short period (1–4 weeks) where a specific set of tasks is completed.
- Develop and Test: Build and test the features during the sprint.
- Get Feedback: Show the progress to customers or stakeholders at the end of the sprint.
- Repeat: Use the feedback to plan the next sprint and improve the software.

### Disadvantages - 
- Requires Skilled Teams: Relies on experienced teams for success.
- Less Predictability: Hard to estimate timelines and budgets due to changing requirements.
- Limited Documentation: Focus on working software may lead to insufficient documentation.
- Time-Consuming Meetings: Frequent meetings can take up significant time.
- Scope Creep: Continuous changes may lead to uncontrolled growth in project scope.

# DevOps -
- DevOps Model is a software development approach that combines Development (Dev) and Operations (Ops) teams to work collaboratively throughout the entire software development lifecycle.
- The goal of DevOps is to increase the speed, quality, and efficiency of delivering software by fostering communication, automation, and continuous delivery.

![17358827664026135776453411519694](https://github.com/user-attachments/assets/3c98539b-06c5-41a4-b1fc-dfee5ec5a552)


## CICD -
- Continuous Integration (CI):
     - Developers frequently commit code changes to a shared repository, and automated tests are run to ensure quality.

- Continuous Delivery (CD):
    - Code is automatically prepared for deployment, ensuring that new features and fixes can be released quickly.
 
- Automation:
    - Automate repetitive tasks (e.g., testing, deployment) to speed up processes and reduce human error.

- Monitoring and Feedback:
   - Continuous monitoring of the application in production helps detect issues and gather feedback, which is then used to improve future releases.

### Advantages -
- Faster Delivery: Continuous integration and delivery speed up releases.
- Improved Collaboration: Development and operations work closely together.
- Continuous Feedback: Real-time feedback ensures quick fixes and improvements.
- Automation: Reduces manual effort and human error.
- Adaptability: Easily accommodates changing requirements.
- Higher Quality: Continuous testing ensures better quality control.
- Risk Reduction: Small updates reduce the risk of major failures.
- Resource Efficiency: Optimizes tasks and resources.
- Scalability: Easily scales to meet growing demands.


# Monolithic vs Microservices -
## Monolithic Architecture -
- Monolithic architecture is a design where an entire application is built as a single unit.
- All the features (e.g., user interface, database, business logic) are tightly connected and work together as one program.
- Example: A single app that handles user login, product listings, payments, and order tracking all in one place.

## Microservices - 
- Microservices is a design where an application is divided into smaller, independent services.
-  Each service handles one specific feature or function (e.g., login, payments).
-  These services communicate with each other through APIs.
-  Example: A shopping app where one service manages user accounts, another handles payments, and another tracks orders, all working together but independently.




