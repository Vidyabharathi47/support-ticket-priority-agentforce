# Customer Support Ticket Priority Prediction and Automated Assignment System Using Agentforce

A Salesforce-based solution that automatically detects the urgency of customer support tickets, sets their priority, assigns them to an agent, and creates follow-up tasks for urgent cases.

## Problem Statement
Customer support teams receive a large number of tickets every day, but prioritization and assignment are mostly manual. This causes delays in resolving critical issues, incorrect prioritization, uneven workload distribution, and poor customer satisfaction.

## Solution
The system stores tickets in a custom Salesforce object. An Autolaunched Flow reads each ticket description, detects urgency from keywords, sets the priority (High / Medium / Low), assigns the ticket to an agent, and creates a Task for High priority tickets. An Agentforce agent exposes this Flow so users can run it through a conversation.

## Features
- Custom object **Support Ticket Intelligence** to track tickets
- Automatic priority detection from the ticket description
- Automatic assignment to a support agent
- Task creation for High priority tickets
- Output message summarizing the result
- Agentforce agent with the topic **Support Ticket Priority AI**
- Reports and dashboards for managers (status, priority, workload)

## Tools and Technologies
Salesforce (Developer Org), Custom Objects and Fields, Salesforce Flow (Autolaunched Flow), Agentforce, Reports and Dashboards

## Data Model
Object: **Support Ticket Intelligence**

| Field | Type | Description |
|---|---|---|
| Ticket Number | Auto Number (TKT-{0000}) | Record name |
| Customer | Lookup (Account) | Customer who raised the ticket |
| Description | Long Text Area | Problem described by the customer |
| Priority Level | Picklist | High, Medium, Low |
| Status | Picklist | New, In Progress, Closed |
| Assigned To | Lookup (User) | Agent handling the ticket |

See [data-model.md](data-model.md) for details.

## Flow Logic
| Description contains | Priority | Extra action |
|---|---|---|
| `urgent` | High | Create Task for the agent |
| `slow` | Medium | None |
| anything else | Low | None |

In every case the Flow sets Status to In Progress, assigns the ticket to an agent, and returns an output message. See [flow-design.md](flow-design.md).

## Test Results
| Input description | Expected priority | Result |
|---|---|---|
| urgent issue | High | Pass |
| system slow | Medium | Pass |
| general query | Low | Pass |

See [test-results.md](test-results.md).

## Screenshots
| Screen | File |
|---|---|
| Object and fields | `screenshots/01-object-fields.png` |
| Custom tab | `screenshots/02-tab.png` |
| Sample data | `screenshots/03-sample-data.png` |
| Flow canvas | `screenshots/04-flow.png` |
| Flow debug result | `screenshots/05-flow-debug.png` |
| Agent topic and action | `screenshots/06-agent-topic.png` |
| Agent test results | `screenshots/07-test-results.png` |

## Demo Video
[Add your demo video link here]

## Documentation
- [requirements.md](requirements.md): business requirements, scope, user needs, tools, security model
- [data-model.md](data-model.md): object and field design
- [flow-design.md](flow-design.md): Flow and Agentforce configuration steps
- [test-results.md](test-results.md): test cases and results

## Team
- Vidya Bharathi (Team Lead)
- Sahaya Esther (Member)
