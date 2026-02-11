# Code Changes for pan-gp-leef-vpn-login-success-gatewayprelogin (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['"host":"({host}[^"]+)"', 'DeviceName=({host}[\w\-.]+)(\s\w+=|\|)'] |