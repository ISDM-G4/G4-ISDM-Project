# Use Case Respond to Interactive Voice Unit

**Use Case ID** | UC#106: Respond to Interactive Voice Unit
**User Story** | As a relationship manager (RM) I want the automated voice system to solicit basic information from customers so that I won't talk to them without any knowledge.
**Goal** | Customers should answer questions from the Interactive Voice Unit to supplement RM knowledge.
**Priority** | High
**Actors** | Primary Actor: Customer<br>Secondary Actor: Relationship Manager
**Pre-conditions** | The customer has called the agency. The Interactive Voice Unit has been enabled and configured with questions.
**Post-conditions** | The customer has successfully answered questions.
**Trigger** | The customer calls the agency.
**Main Flow** | 1. The customer on call is routed to the Interactive Voice Unit.<br>2. The customer hears the pre-recorded messages from the Unit.<br>3. The customer responds to each question by inputting on their phone's keypad.<br>4. Steps 2-3 are repeated until all questions are answered.<br>5. The Interactive Voice Unit records the responses and thanks the customer for their time.<br>6. The customer's session with the Unit ends, and they are routed to the main queue.<br>7. The use case ends.
**Exceptions** | Exception 1, Step 1-6: If the customer ends the call at any time.<br>Exception 2, Step 2-3: The customer does not press any input on their keypad.
**Includes/Extends/Inherits** | Includes **UC#102: Store Customer Details**
**Supporting Information** | Voice responses are retrievable by Relationship managers.
**Non-functional Requirements** | Performance: Routing time when switching to and from the Unit.<br>