# Code Changes for cyberark-pam-cef-app-login-fail-userauth (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | event_code | ['Cyber-Ark|Vault\|[^\|]+\|({event_code}\d+)'] | ['Cyber-Ark\|Vault\|[^\|]+\|({event_code}\d+)'] |