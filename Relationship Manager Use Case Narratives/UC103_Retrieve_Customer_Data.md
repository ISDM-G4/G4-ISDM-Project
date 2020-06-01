# Use case name: Retrieve Customer Data

Header | Info
--- | ---
**Use Case ID** | UC103: Retrieve customer data
**User Story** | As a relationship manager I want customer and package details provided to me for outbound customer calls so that I can immediately engage with the customer.
**Goal** | Retrieve customer data
**Priority** | H 
**Actors** | Primary Actor – Relationship manager (RM)<br>Secondary Actor – Database
**Pre-conditions** | The RM has a unique ID to log into the system<br>The RM has authority to access customer information database
**Post-conditions** | The RM has retrieved the requested customer data
**Trigger** | RM requires information
**Main Flow** | 1. RM logs in with unique ID<br>2. RM clicks customer data tab<br>3. System generates a list of all customers<br>4. RM filters customers based on personal customer information eg. Age, gender, ethnicity, travel interests<br>5. Alternate Flow 1<br>6. System returns the list of filtered customers<br>7. RM choses a customer<br>8. System returns all customer data on that customer<br>9. The use case ends.
**Exceptions** | Exception1. Step 1 – If the CMC system in not available and the system is down.<br>Exception2. Unauthorised user attempts to access the database<br>Exception3. No internet
**Includes/Extends/Inherits** | 
**Supporting Information** | 
**Non-functional Requirements** | Performance: Page load time<br>Security: Only privileged employees can access customer data

Header | Info
--- | ---
**Alternate Flow 1** | “Manual choosing”  
**Trigger** | RM chooses this option if they have a customer in mind
**Step** | 1. RM searches for a specific customer<br>2. Step 8 of Main flow
**Post-conditions** | The database has listed customers suitable for the RM  
**Exceptions** | Exception1.