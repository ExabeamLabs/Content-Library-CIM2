# Code Changes for checkmarx-checkm-json-app-login-fail-failedlogin (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | failure_reason | ['exa_json_path=Details,exa_regex=\\?"Details\\?":\s*\\?"({failure_reason}[^"]+?)\\?"'] | ['exa_json_path=$.Details,exa_regex=\\?"Details\\?":\s*\\?"({failure_reason}[^"]+?)\\?"'] |