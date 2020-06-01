# Use case Call the Agency

**Header** | **Info**
--- | ---
**Use Case ID** | UC#114: Call the agency
**User Story** | As a customer I want to be routed quickly to a relationship manager so that I don't waste time waiting for a connection.
**Goal** | The customer should be eventually routed to an RM as soon as possible.
**Priority** | High
**Actors** | Primary Actor - Customer<br>Secondary Actor - Call management system
**Pre-condtions** | No pre-conditions
**Post-conditions** | The customer is classified as an Inbound Customer
**Trigger** | The agency's number is called.
**Mainflow** | 1. The customer is connected to the Call Management Centre system.<br>2. The system performs a look-up on the customer's phone number and attempts to retrieve customer information.<br>3. The system uses the existing information to re-profile the customer.<br>4. The system determines the customer's target package and calculates a purchase probability metric (purchase score).<br>5. If the Voice Interactive Unit is enabled, the customer is routed to it, otherwise they are routed to the main queue.<br>6. The use case ends.
**Exceptions** | Exception 1, Step 2: No customer profile is found in the database.
**Includes/Extends/Inherits** | Includes **UC#102 Match Customer with RM based on Profile**, **UC#105 Respond to Interactive Voice Unit**, **UC#115 Wait in Queue**
**Supporting Information** | Calls are only accepted during operating hours. Calls outside of these hours will be met with an automated explanation message and disconnection.
**Non-functional Requirements** | Performance: Retrieval and score calculation is done quickly to minimise wait time.

**Header** | **Info**
--- | ---
**Alternate Flow 1** | "No customer profile found"
**Trigger** | The system does not find any profile related to the customer's phone number.
**Step** | 1. The system initialises a new empty profile for the customer and selects a random target package.<br>2. The system determines a lowly-weighted purchase score.<br>3. Re-join the main flow at Step 5.
**Post-conditions** | The system successfully initialises a customer profile.
**Exceptions** | None.
