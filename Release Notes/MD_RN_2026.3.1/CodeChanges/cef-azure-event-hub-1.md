# Code Changes for cef-azure-event-hub-1 (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | operation |  | ['CEF:([^\|]*\|){5}({operation}[^\|]+)', '\Wact=({operation}[^=]+)\s+(\w+=|$)', '\WflexString1=({operation}[^=]+)\s+(\w+=|$)'] |