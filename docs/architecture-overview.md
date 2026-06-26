# Architecture Overview

This project demonstrates a modern HR integration architecture connecting a synthetic HRIS workflow, an integration API, AI enrichment, and Salesforce.

## High-Level Flow

1. Candidate data is entered through a synthetic HRIS user interface.
2. The integration layer receives the candidate payload.
3. Candidate data is stored in a database.
4. An AI service generates a recruiter-facing summary.
5. The integration layer publishes the enriched candidate record to Salesforce.
6. Salesforce stores the final record in a custom `Candidate__c` object.

## Architectural Pattern

This follows a common enterprise integration pattern:

- System of entry: Synthetic HRIS UI
- Integration layer: Node.js / Express API
- Data layer: PostgreSQL
- AI enrichment layer: Ollama / local LLM
- System of engagement: Salesforce

## Salesforce Object

The Salesforce custom object used in the demo is:

`Candidate__c`

Key fields:

- Candidate Number
- First Name
- Last Name
- Email
- Desired Role
- Candidate Status
- AI Summary