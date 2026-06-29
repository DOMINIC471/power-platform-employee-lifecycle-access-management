# Power Platform Employee Lifecycle Access Management

## Overview

This project showcases a Microsoft Power Platform solution developed at SEUPB to manage IT access requests across the employee lifecycle, including new joiners, role changes/movers, and leavers.

The solution replaces a manual Word document and email-based process with a centralised Power Apps form, SharePoint-backed data model, automated approval routing, generated IT checklists, and automated IT ticket notifications.

> Portfolio note: This repository is a sanitised case study. Screenshots, diagrams, sample data, and snippets are either recreated, anonymised, or reviewed before publication.

## Problem

Previously, HR completed IT access information using a Word document, emailed approvers individually, and separately raised IT setup requests. This created several issues:

- Manual follow-up with multiple approvers
- Limited visibility of approval progress
- No central audit trail for access decisions
- IT had to manually interpret build/access requirements
- No automatic setup/offboarding checklist
- Risk of missing setup or removal tasks
- Longer processing time for onboarding, movers, and leavers

## Solution

The solution centralises the IT access request process in Power Apps and automates the supporting workflow using Power Automate and SharePoint Lists.

HR submits the request once through Power Apps. The system then:

- Creates approval transaction records
- Routes approval requests to the correct approvers
- Tracks approval/rejection decisions
- Generates IT checklist records
- Creates checklist items based on request type and build type
- Sends a structured notification to IT
- Maintains records for audit and tracking

## Main Users

- HR users: create and submit access requests
- Approvers: approve or reject requested access via Teams/Outlook
- IT users: manage and complete generated checklist tasks

## Request Types

The app supports:

- New Joiner
- Role Change / Mover
- Leaver

## Technologies Used

- Microsoft Power Apps
- Microsoft Power Automate
- SharePoint Lists
- Microsoft Approvals
- Microsoft Teams / Outlook approvals
- Microsoft 365 Groups
- Office 365 Users / Groups connectors

## Key Features

### Power Apps Front End

- Central request form for HR
- Request type selector for New Joiner, Role Change, and Leaver
- Separate HR, Approver, and IT sections
- Role-based access/editing logic
- Deep linking into specific requests and sections
- Searchable request gallery
- Manual refresh option for updated status

### Approval Automation

- Access requirements are mapped to approver roles
- Approval transaction records are generated automatically
- Approvers receive approval requests through Microsoft Approvals
- Approved/rejected decisions are written back to SharePoint
- Rejected requests are returned for rework

### IT Checklist Automation

- IT checklist parent records are created automatically
- Checklist items are generated based on request type and build type
- Mover requests generate delta tasks
- Leaver requests generate offboarding and equipment return tasks
- Progress percentage is calculated automatically

### Ticketing Notification

- Structured notification emails are sent to IT
- The email includes relevant request details and a Power Apps deep link
- Duplicate ticket emails are prevented using a sent flag

## Data Model

The solution uses SharePoint Lists for:

- Access request records
- Approver directory records
- Approval transaction records
- IT checklist parent records
- Checklist task records

See `documentation/data-model.md` for more detail.

## Impact

The solution significantly reduced manual administration and improved visibility, consistency, and auditability.

Estimated benefits:

- Reduced manual HR follow-up
- Faster processing of IT access requests
- Clearer approval tracking
- More consistent IT setup/offboarding checklist generation
- Reduced risk of missed IT tasks
- Improved audit trail across request, approval, and checklist stages

Previously, processing could take around 1-2 weeks depending on manual follow-up, approver availability, and manual IT interpretation. With automation and clearer routing, the process can potentially be completed in around 1-3 days where approvals and IT actions are completed promptly.

## Confidentiality

This repository does not include:

- Real employee records
- Real personal data
- Internal tenant IDs
- Internal environment IDs
- Internal SharePoint URLs
- Production exported app packages
- Production exported flow packages
- Confidential internal documentation
