# Use case Prioritise Queue

**Header** | **Footer**
--- | ---
**Use Case ID** | UC#108: Prioritise Queue
**User Story** | As the travel agency owner I want the new call system to prioritise customers who are more likely to purchase packages so that I can increase turn over efficiency.
**Goal** | Prioritise the customer queue based on purchase probability.
**Priority** | Low
**Actors** | Main Actor - Call management system<br>Secondary Actor - Customer
**Pre-conditions** | There are customers in the queue.
**Post-conditions** | The queue is sorted
**Trigger** | A customer was recently added to the queue.
**Main Flow** | 1. If a customer was added to the queue, the system looks up their profile and uses their purchase score as a sorting metric.<br>2. The system inserts the customer into their proper place in the queue, sorting from most probable to buy a package (highest purchase score) to least probable to buy a package (lowest purchase score)<br>3. Use case ends.
**Exceptions** | Exception1, Step2: Newly added customer has same purchase score as another customer(s) in the queue. The customer is inserted behind them, giving priority to customers already waiting in the queue.
**Includes/Extends/Inherits** | Extends **UC#115 Wait in queue**
**Supporting Information** | The queue is purely computational, meaning customers aren't physically placed into a queue. The system puts all customer's calls on hold, and then uses the queue as a reference for which customer to route first.
**Non-functional Requirements** | Reliability: The queue sorting mechanism provides increased efficiency in customer turn over.