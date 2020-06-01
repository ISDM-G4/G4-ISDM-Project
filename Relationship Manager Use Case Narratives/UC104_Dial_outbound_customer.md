# Use case name: Dial Outbound Customer

Header | Info
--- | ---
**Use Case ID** | UC104: Dial outbound customer
**User Story** | As a relationship manager I want outbound calls to be automatically dialed by the system so that I can focus on sales and not dailing numbers from a list.
**Goal** | Dial potential customers
**Priority** | H
**Actors** | Primary Actor – Relationship manager (RM)<br>Secondary Actor – Customer
**Pre-conditions** | The RM has a unique ID to log into the system<br>The RM has authority to access customer information database
**Post-conditions** | The RM has access and reviewed customer responses 
**Trigger** | RM calls a customer
**Main Flow** | 1.	RM logs in with unique ID<br>2.	The system generates an outbound customer list based on potential packages and matching attributes, sorted by purchase probability.<br>3. When ready, the RM clicks to call a new outbound customer.<br>4. The system automatically dials and connects the outbound customer to the RM.<br>5. End of use case
**Exceptions** | Exception1. Step 1 – If the CMC system in not available and the system is down.<br>Exception2. Phone lines are down<br>Exception3. No internet
**Includes/Extends/Inherits** | Included by UC102 Populate outbound queue
**Supporting Information** | 
**Non-functional Requirements** | Performance: Page load time<br>Security: Only privileged employees can access customer data