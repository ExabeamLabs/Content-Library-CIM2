# Code Changes for microsoft-azure-sk4-alert-trigger-success-security (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | operation |  | ['"operationName":"({operation}[^"]+)"', 'CEF:([^\|]*\|){5}({operation}[^\|]+)', '\Wact=({operation}[^=]+)\s+(\w+=|$)', '\WflexString1=({operation}[^=]+)\s+(\w+=|$)'] |