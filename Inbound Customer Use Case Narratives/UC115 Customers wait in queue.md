# Use case Wait in queue

**Header** | **Info**
--- | ---
**Use Case ID** | UC#115: Wait in Queue
**User Story** | As a customer I want to be routed quickly to a relationship manager so that I don't waste time waiting for a connection.
**Goal** | Minimise the time customers are on hold when waiting for an RM connection.
**Priority** | High
**Actors** | Primary Actor - Customer<br>Secondary Actor - Call management system
**Pre-conditions** | The customer has called the agency.<br>All available relationship managers are busy.
**Post-conditions** | Customer has awaited an RM connection.
**Trigger** | After the customer has called the agency but all available relationship managers are currently busy.
**Main Flow** | 1. A pre-recorded message explains to the customer that all relationship managers are busy and that they will be put in queue.<br>2. Simple background music plays whilst the customer is waiting to highlight that the call is still live.<br>3. When the system has determined it is the customer's turn (based on priority) and a suitable RM is available, the customer is re-routed to the RM.<br>4. End of use case.
**Exceptions** | Exception1, Steps 1-2: If the customer ends the call whilst waiting in queue, they are dropped and their purchase score lowered.
**Includes/Extends/Inherits** | Included by **UC#114 Call the agency**<br>Includes **UC#116 Disconnect call**<br>Extended by **UC#108 Prioritise Queue**
**Supporting Information** | The queue is capable of holding as many customers as possible, limited only by hardware.<br>The queue is purely computational, meaning customers aren't physically placed into a queue. The system puts all customer's calls on hold, and then uses the queue as a reference for which customer to route first.
**Non-functional Requirements** | Reliability: The queue should function 99% of the time so that no (or very few) customers are unintentionally dropped.