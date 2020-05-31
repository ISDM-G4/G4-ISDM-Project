# Use case Store Customer Responses

**Header** | **Info**
--- | ---
**Use Case ID** | UC#106: Store customer responses
**User Story** | As a relationship manager I want the automated voice system to solicit basic information from customers so that I won't talk to them without any knowledge.
**Goal** | Customer responses should be stored and accessible to RMs to they can engage more quickly with customers.
**Priority** | High
**Actors** | Primary Actor - Call management system<br>Secondary Actor - Relationship Manager, Database Engineer, Customer
**Pre-conditions** | The Customer has successfully answered questions with the Interactive Voice Unit.
**Post-conditions** | The responses are retrievable by Relationship Managers.
**Trigger** | The customer has finished answering the Interactive Voice Unit and have been routed to the queue.
**Main Flow** | 1. The system checks that the responses to the questions exist.<br>2. The system stores these responses in the database for later retrieval by Relationship Managers.<br>3. Use case ends.
**Exceptions** | Exception1. Step 1: The system does not find any responses, or the responses are corrupted.
**Includes/Extends/Inherits** | Included by **UC#105 Respond to Interactive Voice Unit**
**Supporting Information** | A database engineer is flagged when the system faults at Exception1.
**Non-functional Requirements** | Security: Corruption is flagged