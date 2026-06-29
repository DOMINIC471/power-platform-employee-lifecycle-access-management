# Workflow Overview

## 1. HR Request Creation

HR creates a request in Power Apps and selects the request type:

- New Joiner
- Role Change / Mover
- Leaver

## 2. Approval Transaction Generation

The app calls a Power Automate flow to generate approval transaction records based on selected access requirements.

## 3. Approval Processing

A separate flow creates Microsoft approval requests and waits for approver responses.

## 4. Checklist Creation

Once access is approved, IT checklist parent records and checklist items are generated.

## 5. IT Ticket Notification

A structured email notification is sent to IT with the relevant request details and a deep link to the Power App.

## 6. IT Completion Tracking

IT completes checklist items. Checklist progress is updated automatically.
