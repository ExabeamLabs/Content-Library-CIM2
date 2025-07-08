# Code Changes for microsoft-azuread-cef-app-login-clientappused (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | browser | ['"browser":"(|({browser}[^"]+))"'] | ['"browser":"({browser}[^\d\"]+?)\s*([\d\.]+)?"'] |