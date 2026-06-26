# Salesforce Setup

This demo uses Salesforce Developer Edition with a custom object and OAuth-based API authentication.

## Custom Object

Object:

`Candidate__c`

Fields:

- Candidate Number
- First Name
- Last Name
- Email
- Desired Role
- Candidate Status
- AI Summary

## OAuth Configuration

The integration uses a Salesforce External Client App / Connected App configured for OAuth 2.0.

Required OAuth scopes:

- Manage user data via APIs
- Perform requests at any time

The application authenticates to Salesforce before publishing candidate records through the Salesforce REST API.

## Salesforce Role in the Architecture

Salesforce acts as the system of engagement where enriched candidate data is stored and viewed by business users.