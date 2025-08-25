# Code Changes for microsoft-windows-endpoint-login-fail-5 (Event Builder)

| Code Change | Field Name | 2025.14.1 | 2025.15.1 |
|-------------|------------|-----------|------------|
| edit_conditions | expression | InList(type,'microsoft-windows-cef-endpoint-login-device') && !InList(tolower(result), 'logonsuccess') | InList(type,'microsoft-windows-cef-endpoint-login-device') && !InList(tolower(result), 'logonsuccess', 'logonattempted') |