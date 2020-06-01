**Use Case Narrative**

**Use Case Name: Buy Ticket**

| **Use Case ID** | UC101: Access customer response |
| --- | --- |
| **User Story** | As a Relationship manager, I want to access the database to review the customers&#39; responses |
| **Goal** | Access customer responses |
| **Priority** | H |
| **Actors** | Primary Actor – Relationship manager (RM)Secondary Actor – Database |
| **Pre-conditions** | The RM has a unique ID to log into the systemThe RM has authority to access customer information database |
| **Post-conditions** | The RM has access and reviewed customer responses |
| **Trigger** | RM logs into the system |
| **Main Flow** |
1. RM logs in with unique ID
2. RM clicks customer data tab
3. System generates a list of all customers
4. RM filters customers based on personal customer information eg. Age, gender, ethnicity, travel interests
5. Alternate flow 1
6. System returns the list of chosen customers
7. RM accesses individual responses
8. The use case ends.
 |
| **Exceptions** |
1. If the CMC system in not available and the system is down
2. Unauthorised user attempts to access the database
3. No internet
 |
| **Includes/Extends/Inherits** | |
| **Supporting Information** |
 |
| **Non-functional Requirements** | Performance: Page load timeSecurity: Only privileged employees can access customer data |

| **Alternate Flow 1** | &quot;Automated choosing&quot; |
| --- | --- |
| **Trigger** | RM chooses this option instead of manual filtering |
| **Step** |
1. RM instructs system to automated filter responses
2. System returns a list of customers based on the RM&#39;s profile
3. Step 6 of Main flow
 |
| **Post-conditions** | The database has listed customers suitable for the RM |
| **Exceptions** | Same as above |

| **Use Case ID** | UC102: Populate outbound queue |
| --- | --- |
| **User Story** | As a Relationship manager, I want the system to populate an outbound queue |
| **Goal** | Populate outbound queue |
| **Priority** | H |
| **Actors** | Primary Actor – Relationship manager (RM)Secondary Actor – Database |
| **Pre-conditions** | The RM has a unique ID to log into the systemThe RM has authority to access customer information database |
| **Post-conditions** | The RM has access and reviewed customer responses |
| **Trigger** | RM logs into the system |
| **Main Flow** |
1. RM logs in with unique ID
2. RM clicks populate outbound queue
3. System generates a calling queue of customers
4. RM calls customers
5. The use case ends
 |
| **Exceptions** |
1. If the CMC system in not available and the system is down.
2. Phone lines are down
3. No internet
 |
| **Includes/Extends/Inherits** | IncludesExtended by UC104: Dial outbound customer |
| **Supporting Information** |
 |
| **Non-functional Requirements** | Performance: Page load timeSecurity: Only privileged employees can access customer data |

| **Use Case ID** | UC103: Retrieve customer data |
| --- | --- |
| **User Story** | As a Relationship manager, I want to retrieve specific customer data |
| **Goal** | Retrieve customer data |
| **Priority** | H |
| **Actors** | Primary Actor – Relationship manager (RM)Secondary Actor – Database |
| **Pre-conditions** | The RM has a unique ID to log into the systemThe RM has authority to access customer information database |
| **Post-conditions** | The RM has retrieved the requested customer data |
| **Trigger** | RM requires information |
| **Main Flow** |
1. RM logs in with unique ID
2. RM clicks customer data tab
3. System generates a list of all customers
4. RM filters customers based on personal customer information eg. Age, gender, ethnicity, travel interests
5. Alternate Flow 1
6. System returns the list of filtered customers
7. RM choses a customer
8. System returns all customer data on that customer
9. The use case ends.
 |
| **Exceptions** |
1. If the CMC system in not available and the system is down.
2. Unauthorised user attempts to access the database
3. No internet
 |
| **Includes/Extends/Inherits** |
 |
| **Supporting Information** |
 |
| **Non-functional Requirements** | Performance: Page load timeSecurity: Only privileged employees can access customer data |

| **Alternate Flow 1** | &quot;Manual choosing&quot; |
| --- | --- |
| **Trigger** | RM chooses this option if they have a customer in mind |
| **Step** |
1. RM searches for a specific customer
2. Step 8 of Main flow
 |
| **Post-conditions** | The database has listed customers suitable for the RM |
| **Exceptions** | Same as above |

| **Use Case ID** | UC104: Dial outbound customer |
| --- | --- |
| **User Story** | As a Relationship manager, I want to access the database to review the customers&#39; responses |
| **Goal** | Dial potential customers |
| **Priority** | H |
| **Actors** | Primary Actor – Relationship manager (RM)Secondary Actor – Customer |
| **Pre-conditions** | The RM has a unique ID to log into the systemThe RM has authority to access customer information database |
| **Post-conditions** | The RM has access and reviewed customer responses |
| **Trigger** | RM calls a customer |
| **Main Flow** |
1. RM logs in with unique ID
2. RM clicks &#39;generate outbound list&#39;
3. System returns a list of potential customers that have matched the RM&#39;s profile
4. RM&#39;s sorts by priority ie. willingness to purchase that the system as calculated
5. RM chooses customer and learns about them
6. RM calls customer
7. The use case ends
 |
| **Exceptions** |
1. If the CMC system in not available and the system is down.
2. Phone lines are down
3. No internet
 |
| **Includes/Extends/Inherits** | IncludesExtended by |
| **Supporting Information** |
 |
| **Non-functional Requirements** | Performance: Page load timeSecurity: Only privileged employees can access customer data |
