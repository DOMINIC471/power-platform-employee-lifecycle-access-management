# Permissions and Governance

## User Roles

- HR users can create and update HR request information.
- Approvers approve or reject access requests.
- IT users manage IT checklist items and complete setup/offboarding tasks.

## Power Apps Permission Logic

The app uses Microsoft 365 group membership checks to determine whether the signed-in user belongs to the HR or IT group.

## Editing Rules

- HR and IT can access HR/Approver sections.
- Only IT can edit the IT section.
- Delete access is restricted to IT.

## Governance Considerations

- Service account ownership should be used for business-critical flows.
- Run-only permissions should be assigned where possible.
- Internal URLs, tenant IDs, and group IDs should not be exposed publicly.
- Flows should have IT co-owners for maintainability.
