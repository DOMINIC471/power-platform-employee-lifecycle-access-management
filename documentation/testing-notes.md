# Testing Notes

## Test Scenarios

The following scenarios should be tested:

### New Joiner Request

- HR creates a new joiner request.
- Required fields are completed.
- Access requirements are selected.
- Approval transactions are generated.
- Approvals are completed.
- Onboarding checklist is generated.
- IT ticket email is sent.
- IT checklist progress updates correctly.

### Role Change / Mover Request

- HR selects Role Change.
- Moving date and updated access requirements are entered.
- Approval process is completed.
- Mover checklist is generated.
- Delta tasks are created for changed access/build requirements.

### Leaver Request

- HR selects Leaver.
- Leaving date is entered.
- Leaver checklist is generated.
- Disable/offboarding tasks are created.
- Equipment return tasks are created where applicable.

### Rejection / Rework

- Approver rejects a request.
- Request status changes to Rework.
- Submitter is notified.
- Request can be updated and resubmitted.

### Permission Testing

- HR user can access HR/Approver sections.
- IT user can access and edit IT section.
- Non-authorised user is blocked from accessing the app.
