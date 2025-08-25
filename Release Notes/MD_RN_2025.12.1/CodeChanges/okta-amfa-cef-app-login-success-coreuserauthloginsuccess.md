# Code Changes for okta-amfa-cef-app-login-success-coreuserauthloginsuccess (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| edit_regex_field | device_id | ['"device":.+?"id":"({device_id}[^"]+)"', 'exa_regex="device":.+?"id":"({device_id}[^"]+)"'] | ['"device":\s*\{[^\}]+"id":"({device_id}[^"]+)"'] |