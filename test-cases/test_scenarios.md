# Support Ticket Intelligence — Test Scenarios

## Objective
Validate support ticket creation, field values, and priority automation in Salesforce.

| Test ID | Scenario | Expected Result |
|---|---|---|
| TC-01 | Create a ticket with valid details | Ticket record is created |
| TC-02 | Enter a ticket subject | Subject is saved correctly |
| TC-03 | Enter a customer name | Customer name is saved correctly |
| TC-04 | Enter a valid customer email | Email is saved correctly |
| TC-05 | Select an issue type | Selected issue type is saved |
| TC-06 | Set the ticket status | Status is saved correctly |
| TC-07 | Set a high-priority ticket matching the Flow conditions | Flow performs the configured action |
| TC-08 | Create a ticket that does not meet the Flow conditions | The configured default behavior is followed |
| TC-09 | Update an existing ticket | Updated values are saved |
| TC-10 | Leave a required field blank | Salesforce displays the configured validation message |

## Test Execution

Record the actual result after running each test in Salesforce.

| Test ID | Actual Result | Status |
|---|---|---|
| TC-01 to TC-10 | Not executed yet | Pending |

## Note
Expected results must be checked against the actual Salesforce field requirements, validation rules, and active Flow configuration.
