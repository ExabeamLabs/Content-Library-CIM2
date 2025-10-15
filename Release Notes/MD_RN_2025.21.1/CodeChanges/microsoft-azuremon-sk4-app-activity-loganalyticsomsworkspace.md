# Code Changes for microsoft-azuremon-sk4-app-activity-loganalyticsomsworkspace (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | event_name |  | ['Activity":"({event_name}[^"]+?)\s*"', 'message":"({event_name}[^"\{}]+?)\s*"'] |