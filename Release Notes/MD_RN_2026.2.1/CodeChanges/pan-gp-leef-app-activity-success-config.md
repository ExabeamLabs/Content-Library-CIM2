# Code Changes for pan-gp-leef-app-activity-success-config (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['"host":"({host}[^"]+)"', 'DeviceName=({host}[\w\-.]+)(\s\w+=|\|)'] |