# Data Model

## New Employee Access Requests

Stores the main HR request record.

Example fields:

- Employee Name
- Job Title
- Team
- Office Location
- Start Date
- Moving Date
- Leaving Date
- Request Type flags
- Access requirement fields
- Submission Status
- Approval Status

## Approver Directory

Stores mapping between access names and approver roles.

Example fields:

- Access Name
- Approver Role
- Is Available
- Primary Approver
- Backup Approver
- Requested Access Names

## Access Approval Transactions

Stores approval instances linked to a request.

Example fields:

- Request ID
- Approver Role
- Assigned To
- Status
- Decision Date
- Comments
- Requested Access Names

## IT Access Checklists

Stores parent checklist records.

Example fields:

- Request ID
- Build Type
- IT Status
- Assigned To
- Checklist Generated
- Percent Complete
- Checklist Type
- Ticket Email Sent

## Checklist Items

Stores individual checklist tasks.

Example fields:

- Task
- Parent Checklist
- Status
- Notes
- Order
- Category
