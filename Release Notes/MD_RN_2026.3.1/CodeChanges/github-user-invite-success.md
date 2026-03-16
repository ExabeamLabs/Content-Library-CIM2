# Code Changes for github-user-invite-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type,'github-g-json-user-invite-success-org', 'github-g-json-user-invite-success-invitemember') && InList(tolower(operation), 'org.invite_member') |