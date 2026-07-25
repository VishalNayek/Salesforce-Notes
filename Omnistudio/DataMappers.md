# Types of Data Mappers : 

### 1. Data Mapper Extract ###

**Purpose**

Extracts data from Salesforce records and converts it into a structured JSON format.

**Used When**

- Sending Salesforce data to an API
- Passing data to an Integration Procedure
- Displaying data in a FlexCard or OmniScript
- We need data from multiple related objects, parent-child relationships, etc.

### 2. Turbo Extract ###

**Purpose:** 

Quickly extracts data from a single Salesforce object with minimal processing.

**Used When**

- We only need fields from one Salesforce object.
- No field transformation is required.
- Performance is the priority.
- You're simply displaying record details in an OmniScript or FlexCard.

### 3. Load ###

**Purpose**
Loads JSON data into Salesforce objects.

**Used When**

- Creating records
- Updating records
- Upserting records

### 4. Transform ###

**Purpose**

Transforms one JSON structure into another JSON structure.
No Salesforce records are involved.

**Used When**

- API request formatting
- API response formatting
- Combining data
- Renaming fields
- Changing data structure

## What is Extraction Object and Extract Object Path ?

**Extraction Object** - This is the Salesforce object that Data Mapper queries.

**Extract Object Path** - This is the name of the JSON node where the extracted data is placed in the output.

**Example** - 

Extraction Object = Account

Extract Object Path = AccountInfo

```json 
{
  "AccountInfo": {
    "Name": "ABC Ltd",
    "Phone": "9999999999",
    "Industry": "Healthcare"
  }
}
```