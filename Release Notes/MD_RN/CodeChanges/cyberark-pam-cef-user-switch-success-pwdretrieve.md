# Code Changes for cyberark-pam-cef-user-switch-success-pwdretrieve (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | event_code | ['CEF:\s*\d+\|([^\|]+\|){3}({event_code}[^\|]+)', 'Cyber-Ark|Vault\|[^\|]+\|({event_code}\d+)'] | ['CEF:\s*\d+\|([^\|]+\|){3}({event_code}[^\|]+)', 'Cyber-Ark\|Vault\|[^\|]+\|({event_code}\d+)'] |