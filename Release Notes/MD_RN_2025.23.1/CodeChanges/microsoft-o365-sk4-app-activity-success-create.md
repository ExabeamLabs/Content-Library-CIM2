# Code Changes for microsoft-o365-sk4-app-activity-success-create (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | event_name |  | ['"Operation":"({event_name}[^"]+?)\.?"', '"op\\*"*:\\*"*({event_name}[^",\\\s]+)', 'CEF:([^\|"]*\|){5}({event_name}[^\|"]+)', '\sflexString1=({event_name}[^=]+?)\.?\s+(\w+=|$)'] |
| removed_attribute | DupFields |  | N/A |