# AI-Powered Text to Query Builder

### Snowflake Streamlit Accelerator using Cortex AI

---

## 1. Overview

The AI-Powered Text to Query Builder is a Snowflake-native Streamlit application that converts natural language questions into Snowflake SQL queries using Snowflake Cortex AI.

This accelerator enables business users, analysts, and executives to interact with enterprise data using plain English, eliminating the need for SQL expertise while maintaining governance, security, and performance.

The solution runs entirely within Snowflake, ensuring no data leaves the platform and all security policies remain enforced.

---

## 2. Business Problem

Organizations face several challenges in enabling self-service analytics:

* Non-technical users lack SQL expertise
* Data teams become bottlenecks
* Slow query turnaround impacts decision-making
* Inconsistent SQL leads to reporting errors
* Increasing data complexity makes querying difficult

These challenges limit true data democratization.

---

## 3. Solution

This accelerator provides an AI-powered interface that:

* Translates natural language into Snowflake SQL
* Understands database and schema context
* Applies SQL best practices
* Maintains governance and security
* Runs entirely within Snowflake

Users select a database and schema, enter a question, and receive a structured SQL query instantly.

---

## 4. Key Features

* Natural Language to SQL conversion
* Schema-aware query generation
* Fully qualified table names
* Readable and formatted SQL output
* Snowflake-native architecture
* Secure Cortex AI integration
* No data movement
* Streamlit-based intuitive UI

---

## 5. Architecture

User Input (Streamlit UI)
↓
Schema Metadata Extraction (Snowflake)
↓
Prompt Engineering with Context
↓
Cortex AI (snowflake-arctic model)
↓
SQL Query Generation
↓
SQL Display in UI

---

## 6. Technical Components

* Snowflake Streamlit
* Snowflake Cortex AI
* Snowpark Python
* Native Snowflake execution
* Metadata-driven prompt generation

---

## 7. Deployment Instructions (Consumer Experience)

### Step 1: Install the Application

* Navigate to **Snowflake Marketplace**
* Search for **AI-Powered Text to Query Builder**
* Click **Get / Install**

---

### Step 2: Open the Application

* Go to **Apps** in Snowsight
* Open **TEXT_TO_SQL_APP_CLEAN**
* Launch:
  **UI → TEXT_TO_QUERY_BUILDER_APP**

> No manual Streamlit setup is required. The UI is included with the application.

---

### Step 3: Grant Access to Your Data (Required)

This application generates SQL queries based on your data.
To allow the app to understand your schema, you must grant access to your database objects.

Run the following commands:

```sql
GRANT USAGE ON DATABASE <your_database> TO APPLICATION ROLE APP_PUBLIC;
GRANT USAGE ON SCHEMA <your_database>.<your_schema> TO APPLICATION ROLE APP_PUBLIC;
GRANT SELECT ON ALL TABLES IN SCHEMA <your_database>.<your_schema> TO APPLICATION ROLE APP_PUBLIC;
GRANT SELECT ON FUTURE TABLES IN SCHEMA <your_database>.<your_schema> TO APPLICATION ROLE APP_PUBLIC;
```

---

### Step 4: Use the Application

1. Select your database and schema
2. Enter a question in plain English
3. Click **Generate Query**
4. View the generated SQL

---

### Important Notes

* The application **does not automatically access your data**
* Access must be explicitly granted by the user
* The app **generates SQL only** and does not execute queries automatically
* This ensures full control and security over your data

---

## 8. Security & Governance

* Runs entirely within Snowflake
* No external data movement
* No credentials stored in code
* Role-based access control enforced
* Full auditability and lineage
* Secure Cortex AI integration

---

## 9. Target Users

* Business Analysts
* Executives
* Data Engineers
* BI Developers
* Citizen Data Scientists

---

## 10. Use Cases

* Self-service analytics
* Executive reporting
* KPI analysis
* Ad-hoc data exploration
* SQL generation and automation

---

## 11. Performance

* Near real-time SQL generation
* Efficient schema-aware prompting
* Snowflake-native performance

---

## 12. Marketplace Positioning

This accelerator is ideal for Snowflake Marketplace distribution as it:

* Demonstrates Cortex AI capabilities
* Enables AI-driven analytics
* Showcases Streamlit-native applications
* Supports enterprise data democratization

---

## 13. Support

For support, enhancements, or deployment assistance, contact the platform engineering team.

---

## 14. License

Internal enterprise accelerator. Redistribution subject to company publishing policies.
