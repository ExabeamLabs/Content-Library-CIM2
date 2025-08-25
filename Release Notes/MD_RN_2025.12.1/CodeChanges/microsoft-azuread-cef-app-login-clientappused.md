# Code Changes for microsoft-azuread-cef-app-login-clientappused (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| edit_regex_field | browser | ['"browser":"(|({browser}[^"]+))"'] | ['"browser":"({browser}[^\d\"]+?)\s*([\d\.]+)?"'] |