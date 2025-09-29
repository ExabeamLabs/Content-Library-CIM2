# Code Changes for okta-amfa-mix-app-login-success-securitycontext (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | device_name |  | ['"target":[^\]]+?"displayName":"({device_name}[^"]+)",[^\]]+?"type":"UDDevice"', '"target":[^\]]+?"type":"UDDevice"[^\]]+?"displayName":"({device_name}[^"]+)",', 'exa_regex="target":[^\]]+?"displayName":"({device_name}[^"]+)",[^\]]+?"type":"UDDevice"', 'exa_regex="target":[^\]]+?"type":"UDDevice"[^\]]+?"displayName":"({device_name}[^"]+)",'] |