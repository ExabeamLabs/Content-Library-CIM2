# Code Changes for github-g-json-user-invite-success-org (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed | Conditions |  | ['"org.', 'action":', 'github_audit'] |
| edit_regex_field | time |  | ['"@timestamp":({time}\d{13}),', '"start":({time}\d{13}),'] |
| edit_attribute | activity_type |  | ['app-activity:success', 'repository-member-add:success', 'repository-member-remove:success', 'user-invite:success'] |