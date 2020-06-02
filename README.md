# G4-ISDM-Project
**Authored by:**

12884843 - Nathan Luu - (Github: nath1100)

13603168 - Daniel - (Github: Danielfont)

12610440 - Paul Le - (Github: G4-Paul-Le)

13559188- Jamane - (Github: Jam-Marcelino)


# Objective outline and problem definition
### Objective
The objective of the project is to improve the operation of the company's call management centre to increase sales efficiency. The project will implement several new functions to the system to achieve this goal, largely involving improving the effectiveness of relationship managers by matching their strengths with calling customers. The new system will also improve rate of calls and allow for flow control to maximise sales per call and reduce expenditure on call times.

### Problem definition
The travel company is in need of a new call management system to improve sales efficiency. Relationship managers (RM) must be matched with customers based on both the RM's stastical profile and the customers. A tool known as the _Profiler tool_ will be used to develop these statistics. The system will use this information to select which RMs should attend to which customers. The new system must also be capable of effectively routing inbound calls depending on the customer's profile, prioritising those that are more likely to purchase packages. During peak times, an _Interactive Voice Response_ unit is required to prompt basic questions before an _Automatic Call Distributor_ routes the call to the first available RM. For outbound calls the system must be able to retrieve a list of potential customers using information from a database and then generate a suitable script for the matching RM that will handle the call.

### Point of View (POV) Statements
The following POV statements reflect the requirements of the new system and its objectives.

- The travel company needs a new call management system that organises their relationship managers based on their skillset so that they can be effectively put to work, as currently relationshp managers with varying skills handle varying customers.

- The travel company with their new call system need to reach out to new potential customers who would not ordinarily call so that they can increase their customer base and thus increase profits.

- Relationship managers who answer calls need to be routed to customers whose travel interests align with their knowledge because they need to make efficient and effective sales of travel packages.

- Relationship managers who answer targeted outbound calls need a prepared script/details generated by the system about the customer because a new customer will more likely stay on call if they are immediately engaged rather than probed with questions.

- Newly hired relationship managers need to have their skillset interpreted by the system so that they can be easily added to the new CMC, as the system will need their profiles to function.

- Customers who call looking for advice need to be paired correctly with skilled relationship managers so that they can receive the information they are looking for.

- Customers who call the agency need to be quickly routed to a human to talk because wasting time waiting for a connection will make them less likely to stay on call.

- Relationship managers need to have the new system prioritise customers who are more likely to purchase a package because much time is wasted with customers who are unlikely to buy with the current system.

- Customers who dial in during busy times need to be routed to an automated voice input system so that they can provide basic information, allowing them to be routed to the correct relationship manager.

- The new system needs to keep statistics on customers in a database so that analysis can be performed to determine which customers are more likely to purchase travel packages and call back/answer.

# Stakeholders
### Major stakeholders
- Travel Company (Product owner)
- Relationship Managers
- End-customers

### Minor stakeholders
- IT/Database engineer
- Call/Routing engineer

### Stakeholder information
**Travel Company (Product owner)** refers to the owner of the travel agency who employs relationship managers. The owner holds a stake in the system due to their ownership of the company and is the client of the software project.

**Relationship Managers** are employees of the travel agency who accept calls/enquiries from customers. Their role is to sell travel packages offered by the travel agency. The function of their role will largely remain similar in the new system but with enhancements to improve sales capability.

**End-customers** are those who seek to purchase travel packages from the agency. Customers are able to call the travel agency and are expected to be routed to a relationship manager to talk to. The new system will improve on this by allowing simple questions to be automatically answered before a relationship manager is connected with the customer.

**IT/Database engineer** is responsible for the handling of data regarding relationship manager statistics (their strengths, field of expertise, etc) and customers. Customer data will be used to measure sale probability. The database engineer is responsible for the management and correction of this private data.

**Call/Routing engineer** is responsible for the operation of the in-house call management centre software. They are responsible for the maintenance of the system (both old and new) and its day to day operation.


# Design Thinking Approach

### How might we (HMW) statements and brainstorming
The following HMW statements are developed from the earlier POV statements. A brainstorming section is added for each HMW statement specifying how each statement can be solved.

- **How might we develop a call management system that will organise currently employed relationship managers based on their strengths and past experiences?**

Relationship managers all have varying past experiences (travelling to different countries, varying cultural background, etc.) so organising them based on valuable assets and skillsets will allow the system to evaluate which relationship managers are best grouped together on shift. The skillsets of RMs on shift together should encompass all (or most) holiday packages being sold by the agency so that all customers can be answered to by a RM. Packages that sell more often should have a greater number of RMs to accommodate for increased customers. The system will quantify the skills of relationship managers based on the properties of packages, such as country/destination, cultural significance, language, attraction type (honeymoon, urban/natural sightseeing, heritage exploration, etc.). The system will generate package scores for each RM based on how many tags/properties match. A higher score signifies a greater understanding/ability to sell the holiday package by the RM.

- **How might we use the call system to bring in new customers that would not ordinarly call themselves?**

Outbound calls are a new feature to the system not present in the current/old system. The goal of outbound calls is to expand the existing customer base. The system will automatically search through a customer database where phone numbers are indexed. Customer details will also be included in this database, such as name, address, and any important data that will aid in the RM's understanding of the customer. During work hours, the system will analyse all RMs on shift and reference the database for potential customers based on available RM skillsets. Each selected customer will then be assigned a holiday package that the system determines they are most likely to purchase. Customers are then prioritised based on purchase probability, and then assigned to RMs on shift depending on RM availability and RM knowledge/skillset (whether the customer's package matches the RM). Each RM will then be queued with their assigned customers. Whenever they are idle, the system will automatically dial the customer for them and direct the call to the RM.

- **How might we match relationship managers with customers based on their interests/skills/experiences?**

Customer data in the database will include tags that are matched with tags in the relationship manager database. RM to customer compatibility will be determined based on these matching properties. Holiday packages that the customer is interested in will contribute significantly to RM-customer matching. Customer type will be determined by the holiday package they are most likely to buy (either inferred by the system or by questions answered by the automatic voice system) and this will be the main factor that matches them to an RM. Customer and RM tag similarity (language, heritage/country of origin, etc) will then be used to decide between which RMs the customer should be matched with should there be multiple RMs on shift who handle the same packages.

- **How might we organise relevant information for relationship managers when we connect them to outbound calls with prospective customers?**

The system will automatically sort through the list of outbound customers and match them with qualified relationship managers. The system will organise which packages the customer is most likely to purchase, which will be known to the relationship manager in advance. Any relevant information regarding the holiday package stored in the system will be given to the relationship manager in advance to supplement their sales effort during the call.

- **How might we add newly hired relationship managers to the system?**

Newly hired relationship managers will have their profiles initialised upon hiring. Basic information such as name, country of origin, date of birth, visited countries, etc. will be input into the system and stored in the database. The system will use this to build their profile and determine which packages the RM is best suited to selling. IT/database engineers will be tasked with adding new RMs to the system.

- **How might we pair customers who call?**

All customers who call in will be organised into a master queue by the system where they are organised based on priority. Customers that are more likely to purchase packages (determined by the system) will be prioritised higher. Each RM on shift will have an inbound call queue. When an RM's queue is empty, the system will assign the next highest priority customer to them taking into account package compatability. Ideally the system will match customers with RMs that are knowledgeable about the package being sold, but during peak hours this efficiency may be lowered to reduce call wait time for customers.

- **How might we route customers between the automated system and relationship managers?**

The automated voice system will help disguise longer customer queue wait times by allowing them to answer basic questions before talking to an RM. The system will query questions to the customers waiting in queue and store this information in the customer database. After these questions are answered, the customer will be eligble for connection to an RM. The call/routing engineer can configure the questions being asked, or if the automated voice system will be used at all (if queue times are already very short, it is better to instantly connect to an RM).

- **How might we organise calling customers based on priority?**

The system will attempt analyse the customer's purchase probability based on current data and past purchases. If they are a repeat customer, they are given higher priority over others. Similarly a regular/previous call record would indicate higher retention, and so they are given higher priority. The accuracy of analysing purchase probability can be enhanced by the automated voice system asking targetted questions, such as asking what the purpose of their call is.

- **How might we solicit information from customers during peak hours using an automated voice system?**

The call/routing engineer will be tasked with setting which questions will be asked by the automated voice system. When a customer calls and is routed to the automatic system, these questions will be presented to them in voice form and require input on caller's number pad.

- **How might we track customer statistics and information to determine purchase probability?**

All statistics and data will be stored in their relevant tables in a database. The database will contain tables for customers, relationship managers, and packages. The database engineer will be tasked with maintaining this database for the system.

# Explain the use of Scrum
Scrum was used to develop the various diagrams and models of the project. The team of four was divided into roles, with Nathan as the scrum master and Paul as the product owner.

The scrum master initially developed a backlog of user stories on Github Issues which was then used to develop the system use case diagram. Each Use case was related to a user story in the backlog (or often multiple), which were divided into two sprints. Due to the limited time remaining upon initiating scrum, the sprint cycles lasted only several days each. During the two cycles, all four members developed use case narratives and diagrams for any key use cases, which was then pushed to Github.

Throughout the scrum cycle, online stand-up meetings were held to evaluate the general progress of the team and bring up any problems in the development of assigned tasks. This was done through the online messaging software Discord.

# Assumptions
The specifications document identifies a database which the call management system will use to store customer, relationship manager, and package data. The document notes the travel company is _major_ in size, meaning it is likely the company has multiple branch offices/agencies located in different areas. Due to this it is unclear whether the database mention is centralised at a datacenter or local to each branch. For this report, it is assumed that the database is housed locally on a branch level, and that the system operates at the branch level as well.

The Interactive Voice Response unit (also referred to as automatic voice system in this report) mentioned in the document specifies that it prompts customers for options and may ask for call reasons. In this report it is assumed that the voice response system interfaces only with calls and involves simple pre-recorded questions. Customers respond to these by pressing numbers on their keypad which the system will wait for. It is further assumed that a call engineer is capable of customising the pre-recorded messages and inputs.

When too many customers call at once, it is assumed they are placed onto a singular sorted queue before being routed to relationship managers whenever they are free/idle.

It is assumed that when a customer calls out of business hours, the system will automatically play a pre-recorded message stating such before rejecting their call.

It is assumed in this report that customers consent to their data being used by the system and stored in the database. For the sake of simplicity, all non-repeat customers who have not have consented to the storing of their data are estimated to have a low purchase probability (and thus lower priority).


# Gain and Risk
In a market saturated with travel agencies offering the same category of products, the process in which it is sold can be the distinguishing factor seperating companies apart creating the competitive edge it needs to be a dominant leader in the industry. The importance of the new information system and the advantage it provides lies in the efficiency and relevance of the data as it is converted into meaningful information. 

What the CMC System will do is sort customers and categorise them based on all types of factors but not limited to; age, gender, enthnicity, travel interests and budget. The system essentially personalises packages for the customer depending on their needs and wants but this is something any company can do. The underlying difference is that the CMC system will also personalise the Relationship Manager's (RM) own profile based on the above factors and match them with similar customers, meaning RM's can tailor make holiday packages based also on personal experience and not relying on automated algorithms like most systems do. The competitive advantage this creates is deeper connection and intimacy between RM and customer which is important in the sales of an expensive product such as this. It also creates a monetary advantage as it manifests loyalty in customers who can trust the expert advice of a human that has tailor made the product, leading to greater potential of not just returning customers but customers willing to purchase.

With all systems problems are inevitable and can only be prevented, treated or minimised. The first effect of a failed system arises if the system is compromised in a way that leaks personal data of the customers including date of birth, credit card numbers and addresses which would most probably lead to a permanent closure of the business. However some lighter, more manageable failures could be in terms of performance where the system processes the data too slowly or inaccurately which means lesser customers or frustrated customers if advertised packages aren't relatable. Failure of the system could also be a negatve return on investment, where the implemented system is not performing as it should be, hence is not meeting the required profits to exceed the cost of implementation.   


# Appendix

### Q and A roleplay with relevant stakeholders

### Analyst/Developer (A) and End user (U)
**A:** What is your main reason for using a travel company?

**U:** I want to receive advice for a holiday or travel destination I have planned. A travel company will help me plan my itinerary.

**A:** Why would you prefer to call the travel company over visiting in person?

**U:** Calling is helpful when I don't have the time to visit or there are no agencies near me.

**A:** What do you expect as a service from the employee answering your call?

**U:** I expect them to be able to help me with any questions I have regarding the travel destination and for them to be knowledgeable enough to give me recommendations if I don't have any in mind.

### Analyst/Developer (A) and Relationship Manager (R)
**A:** What do you prefer about calls over direct customer visits?

**R:** A call allows me to work without any consideraion of the customer, other than what they're saying. I can focus on the work itself.

**A:** What's your biggest problem with the current calling system?

**R:** Often when I answer a call, I am not well equipped to answer their questions as I only have general information prepared beforehand. While I may specialise in specific packages, such as Europe, customers could be calling about Japan or the Phillipines and I would have to quickly bring up material that I'm unfamiliar with.

**A:** What do you expect out of the new system?

**R:** I'd like customers tailored specifically to my skillset, so that I can easily answer their questions without getting flustered trying to bring up materials and details on the package I'm trying to sell. The interactive voice response unit will also give me time to breathe during peak hours, letting customers answer basic questions so I don't have to go through them myself.

### Analyst/Developer (A) and Travel company/Product owner (P)
**A:** What do you expect to gain from this new system?

**P:** I expect a greater efficiency in call turnover rates and employee utilisation, allowing me to hire less relationship managers but have them work to their full potential. The call system should also be fast, as a lot of maintenance costs of the current call system goes to paying for long call times. This should give us a greater profit margin.

**A:** What do you think of the outbound call system?

**P:** I think it's great that it can bring in customers who are on the fence about their travel, or otherwise would have never heard of our agency before. I think it will greatly increase the number of customers we receive.
