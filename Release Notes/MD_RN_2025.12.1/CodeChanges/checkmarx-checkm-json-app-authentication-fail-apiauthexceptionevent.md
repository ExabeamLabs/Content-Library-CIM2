# Code Changes for checkmarx-checkm-json-app-authentication-fail-apiauthexceptionevent (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| edit_regex_field | failure_reason | ['exa_json_path=Details,exa_regex=\\*"(Info|Message)\\*":\s*\\*"({failure_reason}[^"\{\\]+?)\\*"'] | ['exa_json_path=$.Details,exa_regex=\\*"(Info|Message)\\*":\s*\\*"({failure_reason}[^"\{\\]+?)\\*"'] |
| edit_regex_field | resource_path | ['exa_json_path=Details,exa_regex=\\?"RequestPath\\?":\s*\\?"({resource_path}[^"]+?)\\?"'] | ['exa_json_path=$.Details,exa_regex=\\?"RequestPath\\?":\s*\\?"({resource_path}[^"]+?)\\?"'] |