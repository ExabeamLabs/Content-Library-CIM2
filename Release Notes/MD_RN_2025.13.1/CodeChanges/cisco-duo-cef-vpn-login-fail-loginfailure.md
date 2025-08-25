# Code Changes for cisco-duo-cef-vpn-login-fail-loginfailure (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | failure_reason |  | ['"error":\s*"({failure_reason}[^"]+)', '"reason":"({failure_reason}[^"]+)"[^=]+?"result":"(?i)(denied|fraud|failure|error)"'] |