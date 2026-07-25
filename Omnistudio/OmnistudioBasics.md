## What is Omnistudio?

OmniStudio is a low-code Salesforce tool used to build guided customer journeys, integrate data from multiple systems, and create industry-specific digital applications using declarative components instead of custom code.

## Four Pillars of Omnistudio.

 - FlexCards : FlexCards are reusable UI components that display contextual information and allow users to perform actions.
 - DataRaptors : DataRaptors perform data extraction, loading, and transformation between Salesforce objects and OmniStudio components.
 - Omniscript : OmniScript is used to create guided, step-by-step business processes without writing code.
 - Integration Procedures : Integration Procedures orchestrate multiple server-side operations in a single call, improving performance and reducing client-server round trips.

 ## Omnistudio Architecture
 Omnistudio is divided into three main layers.

  1. Digital Experience Layer : This layer is responsible for what the user sees and interacts with. It provides rich, responsive user interfaces and guided experiences. Mainly used for building the UI. It includes - **Flexcards and Omniscripts**.

  2. Service Management Layer : This layer processes data and business logic behind the scenes. It handles data retrieval, updates, and integrations. It includes **DataMappers (Data Raptors) and Integration Procedures.**

  3. Developer Experience Layer : This layer is used for the deployment and management of Omnistudio components between different Salesforce orgs. It helps developers move components (like OmniScripts, FlexCards, and Data Mappers) from one environment to another (e.g., Sandbox to Production).


# Digital Experience Layer (User facing Components)

## FlexCard (OmniStudio)

A **FlexCard** is a component of the **Digital Experience Layer** in OmniStudio.

It is used to display data in a **contextual** and **user-friendly** format. FlexCards allow you to present key information from Salesforce or external systems in a compact, visually appealing way.

### Key Features

- Part of the **Digital Experience Layer**
- Displays data in a contextual and user-friendly format
- Supports built-in controls such as:
  - Action Buttons (for user interactions)
  - Blocks (for grouping information)
  - Charts (for data visualization)
  - Data Tables (for displaying tabular data)
  - And many more
- Enables building rich, interactive user interfaces with **little to no coding**

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
You can build this entire flow using OmniScript, making it easy for users to complete the process without confusion.

# Service Management Layer

## Integration Procedures


