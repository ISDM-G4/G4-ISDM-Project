# Use case name: Populate Outbound queue

Header | Info
--- | ---
**Use Case ID** | UC102: Populate outbound queue
**User Story** | As the travel agency owner I want customers to be targeted in outbound calls so that we can expand our customer base and increase sales.
**Goal** | Populate outbound queue
**Priority** | H
**Actors** | Primary Actor – Relationship manager (RM)<br>Secondary Actor – Database
**Pre-conditions** | The RM has a unique ID to log into the system<br>The RM has authority to access customer information database
**Post-conditions** | The RM has access and reviewed customer responses 
**Trigger** | RM logs into the system
**Main Flow** | 1. RM logs in with unique ID<br>2. RM clicks populate outbound queue<br>3. System generates a calling queue of customers<br>4. RM calls customers<br>5. The use case ends
**Exceptions** | Exception1. Step 1 – If the CMC system in not available and the system is down.<br>Exception2. Phone lines are down<br>Exception3. No internet
**Includes/Extends/Inherits** | Includes UC104: Dial outbound customer
**Supporting Information** | 
**Non-functional Requirements** | Performance: Page load time<br>Security: Only privileged employees can access customer data