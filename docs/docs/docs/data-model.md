# Data Model

## 1. Custom Object
- **Label:** Support Ticket Intelligence
- **Suggested API Name:** Support_Ticket_Intelligence__c
- **Purpose:** Stores and manages customer support tickets.

## 2. Field Definitions
| Field Label | Suggested API Name | Data Type |
| :--- | :--- | :--- |
| Ticket Number | Name | Auto Number (`TKT-{0000}`) |
| Customer | Customer__c | Lookup (Account) |
| Description | Description__c | Long Text Area |
| Priority Level | Priority_Level__c | Picklist |
| Status | Status__c | Picklist |
| Assigned To | Assigned_To__c | Lookup (User) |

*Note: Confirm the actual API names when creating the fields in Salesforce.*

## 3. Picklist Values
### Priority Level
- High
- Medium
- Low

### Status
- New
- In Progress
- Closed

## 4. Relationships
- **Customer:** Lookup relationship to Account.
- **Assigned To:** Lookup relationship to User.
- **Follow-up Task:** A Salesforce Task associated with the relevant ticket and assigned to the responsible user, according to the implemented relationship configuration.

## 5. Sample Record
| Field | Example |
| :--- | :--- |
| Ticket Number | TKT-0001 |
| Customer | Sample Customer |
| Description | Urgent issue: unable to access the application |
| Priority Level | High |
| Status | In Progress |
| Assigned To | Configured Support Agent |

*This is illustrative sample data, not a record from a live Salesforce org.*

## 6. Data Validation
- Priority Level must use the defined picklist values.
- Status must use the defined picklist values.
- Ticket descriptions should be checked for missing or blank values.
- Assigned To should reference a valid Salesforce user.
- Customer should reference an existing Account when required.

## 7. Future Enhancements
- Add ticket category and resolution fields.
- Add escalation reason and resolution time.
- Track assignment history.
- Introduce customer sentiment and SLA indicators.
