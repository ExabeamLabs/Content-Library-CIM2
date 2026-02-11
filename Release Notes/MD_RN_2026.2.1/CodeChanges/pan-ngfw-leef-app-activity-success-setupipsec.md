# Code Changes for pan-ngfw-leef-app-activity-success-setupipsec (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['"host":"({host}[^"]+)"', 'DeviceName=({host}[\w\-.]+)(\s\w+=|\|)'] |