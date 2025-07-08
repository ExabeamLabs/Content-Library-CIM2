# Code Changes for cyberark-pam-cef-user-password-modify-success-vault (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | event_code | ['Cyber-Ark|Vault\|[^\|]+\|({event_code}\d+)'] | ['Cyber-Ark\|Vault\|[^\|]+\|({event_code}\d+)'] |