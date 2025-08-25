# Code Changes for checkmarx-checkm-json-app-login-fail-failedlogin (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| edit_regex_field | failure_reason | ['exa_json_path=Details,exa_regex=\\?"Details\\?":\s*\\?"({failure_reason}[^"]+?)\\?"'] | ['exa_json_path=$.Details,exa_regex=\\?"Details\\?":\s*\\?"({failure_reason}[^"]+?)\\?"'] |