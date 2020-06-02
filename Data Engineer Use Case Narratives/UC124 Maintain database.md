# Use case: Maintain database

**Header** | **Info**
--- | ---
**Use Case ID** | UC#124: Maintain Database
**User Story** | As a database engineer I want to be able to maintain and manage all customer, relationship manager, and package data in the database so that I can update/change them on demand.
**Goal** | To ensure the system keeps functioning and fulfilling the needs of the users
**Priority** | Low
**Actors** | Primary Actor - Database engineer<br>Secondary Actor - Call engineer
**Pre-conditions** | The database is running
**Post-conditions** | Changes to the database are applied
**Trigger** | The database engineer access the database via database management software.
**Main Flow** | 1. The database engineer accesses the database via database management software.<br>2. The engineer edits their intended tables/fields.<br>3. The database engineer applies changes to the database. <br>4. Use case ends.
**Exceptions** | Exception1, Steps 2-3: The database engineer is unable to edit/apply changes due to the data being in use (by an RM or customer service). Instead the changes are queued and applied when the database is no longer being accessed.
**Includes/Extends/Inherits** | 
**Supporting Information** | 
**Non-functional Requirements** | Reliability: Prevents data corruption from multiple user access.
