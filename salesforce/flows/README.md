# Support Ticket Intelligence — Salesforce Flows

## Overview
This folder documents the Salesforce Flows used in the Support Ticket Intelligence project.

## Flow: Ticket Priority Update

- **Purpose:** Automate ticket priority updates based on configured conditions.
- **Object:** Support Ticket Intelligence
- **Status:** Verify the active Flow version in Salesforce Setup before updating this documentation.
- **Automation Type:** Verify whether the Flow is record-triggered or another Flow type.

## Expected Workflow
1. A support ticket record is created or updated.
2. The Flow evaluates the configured conditions.
3. When the conditions match, the Flow updates the ticket's priority.
4. The record is saved with the updated value.

## Verification
Check Salesforce Setup → Flows to confirm the Flow name, trigger conditions, actions, and active version.

## Note
This file is documentation only. The actual Salesforce Flow metadata must be retrieved separately to back up the automation.
