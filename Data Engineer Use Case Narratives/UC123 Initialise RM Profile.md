# Use Case: Initialise RM Profile

**Header** | **Info**
--- | ---
**Use Case ID** | UC#123: Initialise Relationship Manager Profile
**User Story** | As a Database engineer I want all newly hired relationship managers to be easily profiled into the system so that they can go to work quickly.
**Goal** | To create a profile for a Relationship Manager
**Priority** | Medium
**Actors** | Primary Actor - Database engineer<br>Secondary Actor - Relationship manager, Database system
**Pre-conditions** | Profile for the relationship manager does not exist.<br>Relationship manager has completed a profile questionnaire.
**Post-conditions** | Relationship manager profile initialised
**Trigger** | The engineer is requested to initialise the profiles in the database.
**Main Flow** | 1. Receive filled out questionnaire from RM <br>2. Fill out a profile template using information from the questionnaire <br>3. Add the profile to the database.<br>4. End of use case
**Exceptions** | Exception 1, Step 3: The profile is not able to be added to the database due to lack of information. Database engineer requests the RM to fill the questionnaire again.
**Includes/Extends/Inherits** | 
**Supporting Information** | 
**Non-functional Requirements** | 