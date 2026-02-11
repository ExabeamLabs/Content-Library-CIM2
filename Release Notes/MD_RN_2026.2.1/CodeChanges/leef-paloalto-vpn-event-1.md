# Code Changes for leef-paloalto-vpn-event-1 (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['"host":"({host}[^"]+)"', 'DeviceName=({host}[\w\-.]+)(\s\w+=|\|)'] |