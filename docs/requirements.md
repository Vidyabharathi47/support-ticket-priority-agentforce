# Project Requirements

## 1. Project Title
Customer Support Ticket Priority Prediction and Automated Assignment System Using Agentforce

## 2. Objective
To develop a Salesforce-based customer support automation system that identifies ticket urgency, assigns priority levels, routes tickets to support agents, and creates follow-up tasks for high-priority issues.

## 3. Problem Statement
Customer support teams often process large volumes of tickets manually. This can result in delayed responses, incorrect prioritization, uneven workload distribution, and reduced customer satisfaction.

## 4. Proposed Solution
The proposed system uses Salesforce custom objects, Salesforce Flow, and Agentforce to automate ticket processing. The Flow evaluates ticket descriptions using predefined keywords, determines priority, assigns an agent, updates the ticket status, and creates a follow-up task for high-priority tickets. Users can invoke the automation through an Agentforce conversation.

## 5. Functional Requirements
- Create and maintain support ticket records.
- Store customer details, ticket descriptions, priority, status, and assigned agent.
- Identify urgency using predefined keyword rules.
- Classify tickets as High, Medium, or Low priority.
- Assign tickets to an appropriate support agent.
- Update ticket status to In Progress.
- Create follow-up tasks for High priority tickets.
- Return a meaningful processing result to the user.
- Provide reports and dashboards for ticket monitoring.

## 6. Non-Functional Requirements
- Maintain accurate and consistent ticket records.
- Enforce Salesforce access permissions.
- Provide understandable error messages.
- Avoid duplicate follow-up tasks.
- Support maintainable automation and future enhancements.
- Protect customer information.

## 7. Scope
### Included
- Salesforce custom object and fields
- Autolaunched Flow
- Agentforce topic and action
- Priority classification using keyword rules
- Agent assignment
- Task creation
- Reports and dashboards

### Excluded from the Initial Version
- Training a custom machine-learning model
- Integration with external ticketing platforms
- Automatic email or SMS notifications
- Advanced AI-based sentiment analysis

## 8. Technology Stack
- Salesforce Developer Org
- Salesforce Flow
- Agentforce
- Salesforce Reports and Dashboards
- Salesforce DX / Salesforce CLI, where applicable
- Git and GitHub

## 9. Acceptance Criteria
- A ticket can be created and stored successfully.
- Priority is assigned according to the configured rules.
- The ticket is assigned to a valid support agent.
- High-priority tickets generate a follow-up task.
- Agentforce can invoke the configured Flow action.
- Reports display the available ticket data accurately.

## 10. Project Status
Planned / In Progress. Acceptance criteria will be marked complete after implementation and testing.
