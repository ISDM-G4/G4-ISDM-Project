# Use case Disconnect call

**Header** | **Info**
--- | ---
**Use Case ID** | UC#116: Disconnect call
**User Story** | As a customer I want to be routed quickly to a relationship manager so that I don't waste time waiting for a connection.
**Goal** | Customers wait minimal times, but can disconnect at their discretion.
**Priority** | High
**Actors** | Main Actor - Customer<br>Secondary Actor - Call management system
**Pre-conditions** | The customer is waiting in the queue
**Post-condtions** | The customer has disconnected
**Trigger** | The customer disconnects the call, whether accidental or intentional
**Main Flow** | 1. The customer disconnects/ends the call while waiting in the queue.<br>2. The call management system is flagged.<br>3. The call management system removes the customer from the queue and impacts their purchase score.<br>4. The use case ends.
**Exceptions** | No exceptions
**Includes/Extends/Inherits** | Included by **UC#115: Wait in queue**
**Supporting Information** | The call engineer may configure how much the purchase score is impacted (if at all) based on business rules.
**Non-functional Requirements** | Performance: The customer is removed from the queue as soon as possible.
