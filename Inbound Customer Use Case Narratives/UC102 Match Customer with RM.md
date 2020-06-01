# Use case Match Customer with RM

**Header** | **Info**
--- | ---
**Use Case ID** | UC#102: Match customer with RM
**User Story** | As a customer I want my details profiled by the system so that it will match me with a relationship manager that can help me.
**Goal** | To match a customer with a relationship manager based on similar metrics and packages.
**Priority** | High
**Actors** | Primary Actor - Call management system<br>Secondary acctors - Customer, Relationship manager
**Pre-conditions** | The customer has called the agency
**Post-conditions** | The customer has talked with a relationship manager
**Trigger** | After the customer has waited in the queue and their slot has opened with a suitable RM, or the RM is already available.
**Main Flow** | 1. The system determines the customer's suitable RM based on their determined target package. This package is referenced with all on-shift relationship managers to find who specialises in selling this package.<br>2. Of the RMs found, the system references each RM's tags with the customer's tags to find the best match.<br>3. The RM with the most similar/matched tags is selected to be connected.<br>4. The call management system routes the customer to the selected relationship manager and they converse.<br>5. Use case ends.
**Exceptions** | Exception 1, Step 3: Multiple RMs are found with the same amount of similar tags. Alternate flow 1.
**Includes/Extends/Inherits** | Included by **UC114: Call the agency**
**Supporting Information** | 
**Non-functional Requirements** | Performance: Table look-ups by the system should be as fast as possible to minimise lag time.

**Header** | **Info**
--- | ---
**Alternate Flow 1** | "Multiple best-matched RMs"
**Trigger** | After finding multiple package RMs, the system still determines there are multiple best-match RMs based on tags.
**Step** | 1. Out of the remaining best-match RMs, the system performs a comparison check each profile.<br>2. The system sorts the RMs based on most speacialised (low packages) to least specialised (high number of packages).<br>3. The system selects the most specialised RM to match with the customer, leaving the broadly specialised RMs open to other customers.<br>4. Re-join main flow at step 4.
**Post-conditions** | The call management system successfully determines a suitable singular RM to match with the customer.
**Exceptions** | Exception1, Step 3: If the system finds that there are multiple "most specialised" RMs, then the system randomly selects one.