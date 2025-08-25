# Code Changes for cyberark-pam-cef-user-switch-success-pwdretrieve (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| edit_regex_field | event_code | ['CEF:\s*\d+\|([^\|]+\|){3}({event_code}[^\|]+)', 'Cyber-Ark|Vault\|[^\|]+\|({event_code}\d+)'] | ['CEF:\s*\d+\|([^\|]+\|){3}({event_code}[^\|]+)', 'Cyber-Ark\|Vault\|[^\|]+\|({event_code}\d+)'] |