# Code Changes for netskope-sc-json-file-auditlogevent (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A | ['email_address', 'email_domain', 'user'] | ['app', 'email_address', 'email_domain', 'user'] |
| added_regex_field | app | [] | ['exa_regex=({app}netskope)'] |
| edit_attribute | activity_type | ['app-activity:success', 'file-create:success', 'file-delete:success', 'file-download:success', 'file-move:success', 'file-permission-modify:success', 'file-read:success', 'file-rename:success', 'file-upload:success', 'file-write:success', 'folder-delete:success', 'policy-create:success', 'user-create:success'] | ['app-activity:success', 'app-login:success', 'app-logout:success', 'file-create:success', 'file-delete:success', 'file-download:success', 'file-move:success', 'file-permission-modify:success', 'file-read:success', 'file-rename:success', 'file-upload:success', 'file-write:success', 'folder-delete:success', 'policy-create:success', 'user-create:success'] |
| edit_attribute | legacy_activity_type | ['account-creation', 'app-activity', 'file-delete', 'file-download', 'file-permission-change', 'file-read', 'file-upload', 'file-write'] | ['account-creation', 'app-activity', 'app-login', 'file-delete', 'file-download', 'file-permission-change', 'file-read', 'file-upload', 'file-write'] |