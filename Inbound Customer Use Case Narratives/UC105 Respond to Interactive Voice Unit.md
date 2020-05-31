# Use Case Respond to Interactive Voice Unit

**Header** | **Info**
--- | ---
**Use Case ID** | UC#105: Respond to Interactive Voice Unit
**User Story** | As a relationship manager I want customers to be directed to an automatic voice system so that I can handle increased call volumes.
**Goal** | Customers should answer questions from the Interactive Voice Unit to relieve waiting time and burdens on RMs.
**Priority** | High
**Actors** | Primary Actor: Customer<br>Secondary Actor: Call management system
**Pre-conditions** | The customer has called the agency. The Interactive Voice Unit has been enabled and configured with questions.
**Post-conditions** | The customer has successfully answered questions.
**Trigger** | The customer calls the agency.
**Main Flow** | 1. The customer on call is routed to the Interactive Voice Unit.<br>2. The customer hears the pre-recorded messages from the Unit.<br>3. The customer responds to each question by inputting on their phone's keypad.<br>4. Steps 2-3 are repeated until all questions are answered.<br>5. The Interactive Voice Unit records the responses and thanks the customer for their time.<br>6. The customer's session with the Unit ends, and they are routed to the main queue.<br>7. The system re-profiles the customer based on their responses and recalculates their target package and purchase score.<br>8. The use case ends.
**Exceptions** | Exception 1, Step 1-6: If the customer ends the call at any time.<br>Exception 2, Step 2-3: The customer does not press any input on their keypad.
**Includes/Extends/Inherits** | Includes **UC#106: Store Customer Responses**<br>Included by **UC#114 Call the agency**
**Supporting Information** | Voice responses are retrievable by Relationship managers.
**Non-functional Requirements** | Performance: Routing time when switching to and from the Unit.<br>

**Header** | **Info**
--- | ---
**Alternate Flow 1** | "Failed Response"
**Trigger** | The customer does not respond by pressing their keypad.
**Step** | 1. The Interactive Voice Unit stops waiting for a response.<br>2. The Unit asks the customer whether they want to wait for an RM connection or try again.<br>3. If the customer responds to try again, re-join main flow at Step 2. Otherwise rejoin at Step 6 in the main-flow.
**Post Conditions** | The Customer has successfully answered questions.
**Exceptions** | Exception1, Steps 2-3: The customer still does not input a response on their kepad. The call is dropped after further inactivity is detected.