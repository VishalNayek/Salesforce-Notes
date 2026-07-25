## What is Omnistudio?

Omnistudio is a **low-code development tool** built on top of Salesforce. It allows you to create user interfaces (UI), automate business processes, and integrate systems – all without writing much code.

### Why is it used?

- To reduce coding efforts
- To build applications faster
- To create guided user experiences
- To integrate multiple systems easily

**Example: Suppose a telecom company wants to create a new connection request form. Instead of writing custom code, they can use:**

- OmniScript to design the form
- DataRaptor to fetch customer details
- Integration Procedure to validate information
- FlexCards to display plan details
- This makes development faster and easier.

## Four Pillars of Omnistudio.

 - FlexCards : FlexCards are reusable UI components that display contextual information and allow users to perform actions.
 - DataRaptors : DataRaptors perform data extraction, loading, and transformation between Salesforce objects and OmniStudio components.
 - Omniscript : OmniScript is used to create guided, step-by-step business processes without writing code.
 - Integration Procedures : Integration Procedures orchestrate multiple server-side operations in a single call, improving performance and reducing client-server round trips.

 ## Omnistudio Architecture
 Omnistudio is divided into three main layers.

  1. **Digital Experience Layer** : This layer is responsible for what the user sees and interacts with. It provides rich, responsive user interfaces and guided experiences. Mainly used for building the UI. It includes - **Flexcards and Omniscripts**.

  2. **Service Management Layer** : This layer processes data and business logic behind the scenes. It handles data retrieval, updates, and integrations. It includes **DataMappers (Data Raptors) and Integration Procedures.**

  3. **Developer Experience Layer** : This layer is used for the deployment and management of Omnistudio components between different Salesforce orgs. It helps developers move components (like OmniScripts, FlexCards, and Data Mappers) from one environment to another (e.g., Sandbox to Production).


# Digital Experience Layer (User facing Components)

## FlexCard (OmniStudio)

A **FlexCard** is a component of the **Digital Experience Layer** in OmniStudio.

It is used to display data in a **contextual** and **user-friendly** format. FlexCards allow you to present key information from Salesforce or external systems in a compact, visually appealing way.

### Key Features
- Displays data in a contextual and user-friendly format
- Supports built-in controls such as:
  - Action Buttons (for user interactions)
  - Blocks (for grouping information)
  - Charts (for data visualization)
  - Data Tables (for displaying tabular data)
- Enables building rich, interactive user interfaces with little to no coding.

## Omniscripts

OmniScript is a step-by-step guided flow used to collect information from users in a structured way. It allows you to build forms and processes using a drag-and-drop interface, based on business requirements – without writing code.

### Key Features

- Drag-and-drop components
- No coding required (low-code tool)
- Step-by-step user guidance
- Can integrate with Data Mappers and Integration Procedures
- Supports validations and conditional visibility

### Example
Suppose a bank wants to create a Loan Application process:
Step 1 – Enter Personal Details
Step 2 – Enter Employment Details
Step 3 – Upload Documents
Step 4 – Review and Submit
We can build this entire flow using OmniScript, making it easy for users to complete the process without confusion.

# Service Management Layer (Server Side Business Logic)

## Integration Procedures
An Integration Procedure (IP) is used to execute server-side processes in Omnistudio.
It is mainly used when you need to:
- Call multiple data sources
- Apply complex business logic
- Combine responses from different systems
- Perform conditional processing

## DataMapper (Previously known as DataRaptors)
Data Mapper is used to perform data-related operations such as:
- Fetching records (similar to SOQL)
- Inserting records
- Updating records
- Transforming data between different formats
- In simple words, whenever you need to work with Salesforce data, you use Data Mapper.

## Three types of Data Mappers : 

### 1. Data Mapper Extract ###

**Purpose**
Extracts data from Salesforce records and converts it into a structured JSON format.
**Used When**
- Sending Salesforce data to an API
- Passing data to an Integration Procedure
- Displaying data in a FlexCard or OmniScript

### 2. Data Mapper Load ###

**Purpose**
Loads JSON data into Salesforce objects.

**Used When**

Creating records
Updating records
Upserting records

### 3. Data Mapper Transform ###

**Purpose**

Transforms one JSON structure into another JSON structure.
No Salesforce records are involved.

**Used When**

- API request formatting
- API response formatting
- Combining data
- Renaming fields
- Changing data structure






