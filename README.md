# SNHU CS-255 System Analysis and Design Portfolio

This repo houses my CS-255 project (key documents and Q&A covering the course and what I learned).

## Documents

- [Business Requirements Document (Project One)](CS%20255%20Business%20Requirements%20Document%20-%20Thomas%20Archer.docx)
- [System Design Document (Project Two)](CS%20255%20System%20Design%20Document%20-%20Thomas%20Archer.docx)

## Questions & Answers

**Briefly summarize the DriverPass project. Who was the client? What type of system did they want you to design?**

DriverPass was a startup founded by Liam, who identified a gap in the market for comprehensive driver training services. The client wanted a cloud-based web application that would allow students to purchase tiered training packages, take online practice tests, track their progress, and schedule in-person driving lessons with certified instructors. The system also needed to support internal business operations including reservation management, user account administration, activity reporting, and automatic compliance updates from the DMV. The design had to accommodate four distinct user roles, Owner, Administrator, Employee, and Customer, each with their own access permissions and interface.

**What did you do particularly well?**

I think I did particularly well on the requirements gathering and translation phase. My business requirements document was precise about distinguishing functional from nonfunctional requirements, used direct quotes from the interview transcript to justify design decisions, and identified assumptions and limitations explicitly rather than leaving them implicit. That discipline carried through into the system design, where every UML diagram and every technical requirement could be traced back to something a stakeholder actually said. I also think the class diagram demonstrated a stronger understanding of object-oriented design than the assignment required, particularly the decision to model Owner and Administrator as role values within an Employee subclass rather than as separate classes, which more accurately reflects the real-world problem domain.

**If you could choose one part of your work on these documents to revise, what would you pick? How would you improve it?**

I would revise the sequence diagram. While it accurately models the happy path of the Make Reservation use case, it does not model the alternate paths that exist in the activity diagram, specifically what happens when the user declines confirmation or when the selected time slot is no longer available. A sequence diagram that only shows the successful flow gives an incomplete picture of how the system actually behaves, and a developer implementing from that diagram alone would need to make assumptions about the error handling paths. I would add combined fragment blocks to model those alternate flows the same way I used loop and alt fragments in the ATM sequence diagram.

**How did you interpret the user's needs and implement them into your system design? Why is it so important to consider the user's needs when designing?**

I interpreted user needs by treating the interview transcript as the "source of truth" regarding requirements and resisting the temptation to add features or constraints that were not grounded in what the stakeholders actually said. When something was ambiguous, such as the maximum number of failed login attempts before lockout, I documented the ambiguity explicitly and stated my assumption rather than presenting it as a given. I then mapped each stated need to a specific requirement, use case, or design decision so that the connection was always traceable. Considering user needs is not just good practice, it is the entire point of the exercise. A system that is technically elegant but does not solve the problem the client actually has is a failure. Users will not adopt software that does not fit the way they work, and no amount of technical sophistication can compensate for a misalignment between what was built and what was needed.

**How do you approach designing software? What techniques or strategies would you use in the future to analyze and design a system?**

I approach software design iteratively, starting with a thorough understanding of the problem domain before writing a single line of code or drawing a single diagram. In this project that meant reading the interview transcript carefully, identifying the actors and their goals, and building the requirements document before touching any UML tools. Going forward I would continue to use a blended object and process modeling approach, since activity and sequence diagrams together give a more complete picture of system behavior than either alone. I would also invest more heavily in validating requirements with stakeholders before committing to a design, since the most expensive mistakes in software development are the ones discovered late. The discipline of writing requirements in the form of testable shall statements, as I did in the business requirements document, is something I will continue to carry forward because it forces precision and makes it much harder for ambiguity to seep into the implementation phase.