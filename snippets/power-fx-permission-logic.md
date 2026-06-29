# Power Fx Permission Logic

```powerfx
Set(varUserEmail, Lower(User().Email));

ClearCollect(
    colHRGroupMembers,
    Office365Groups.ListGroupMembers(varHRGroupID).value
);

ClearCollect(
    colITGroupMembers,
    Office365Groups.ListGroupMembers(varITGroupID).value
);

Set(
    varIsHR,
    !IsBlank(
        LookUp(
            colHRGroupMembers,
            Lower(Coalesce(mail, userPrincipalName, "")) = varUserEmail
        )
    )
);

Set(
    varIsIT,
    !IsBlank(
        LookUp(
            colITGroupMembers,
            Lower(Coalesce(mail, userPrincipalName, "")) = varUserEmail
        )
    )
);

Set(varCanAccessApp, varIsHR || varIsIT);
Set(varCanEditITSection, varIsIT);
