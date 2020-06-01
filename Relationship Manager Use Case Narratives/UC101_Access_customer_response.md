# Use case name: Access Customer Response

Header | Info
--- | ---
**Use Case ID** | UC101: Access customer response
**User Story** | As a relationship manager I want the automated voice system to solicit basic information from customers so that I won't talk to them without any knowledge.
**Goal** | Access customer responses
**Priority** | H
**Actors** | Primary Actor – Relationship manager (RM)<br>Secondary Actor – Database
**Pre-conditions** | The RM has a unique ID to log into the system<br>The RM has authority to access customer information database
**Post-conditions** | The RM has access and reviewed customer responses 
**Trigger** | RM logs into the system
**Main Flow** | 1. RM logs in with unique ID<br>2. RM clicks customer data tab<br>3. System generates a list of all customers<br>4. RM filters customers based on personal customer information eg. Age, gender, ethnicity, travel interests<br>5. Alternate flow 1<br>6. System returns the list of chosen customers<br>7. RM accesses individual responses<br>8. The use case ends.
**Exceptions** | Exception1. Step 1 – If the CMC system in not available and the system is down.<br>Exception2. Unauthorised user attempts to access the database<br>Exception3. No internet
**Includes/Extends/Inherits** | 
**Supporting Information** | 
**Non-functional Requirements** | Performance: Page load time<br>Security: Only privileged employees can access customer data

Header | Info
--- | ---
**Alternate Flow 1** | "Automated choosing"
**Trigger** | RM chooses this option instead of manual filtering
**Step** | 1.	RM instructs system to automated filter responses<br>2.	System returns a list of customers based on the RM’s profile<br>3.	Step 6 of Main flow
**Post-conditions** | The database has listed customers suitable for the RM  
**Exceptions** | Exception1.Steps1-2 – passenger closes the browser window anytime, and then the OT system blocks the transaction at that point in time and logs the activity.