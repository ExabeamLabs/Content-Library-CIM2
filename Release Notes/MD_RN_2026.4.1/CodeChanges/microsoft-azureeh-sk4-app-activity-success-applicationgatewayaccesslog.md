# Code Changes for microsoft-azureeh-sk4-app-activity-success-applicationgatewayaccesslog (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | event_name |  | ['CEF:([^\|]*\|){5}({event_name}({operation}[^\|]+))', '\Wact=({event_name}({operation}[^=]+))\s+(\w+=|$)', '\WflexString1=({event_name}({operation}[^=]+))\s+(\w+=|$)', 'operationName":"({event_name}({operation}.+?[^\\]))"'] |
| edit_regex_field | operation |  | ['CEF:([^\|]*\|){5}({event_name}({operation}[^\|]+))', '\Wact=({event_name}({operation}[^=]+))\s+(\w+=|$)', '\WflexString1=({event_name}({operation}[^=]+))\s+(\w+=|$)', 'operationName":"({event_name}({operation}.+?[^\\]))"'] |
| edit_regex_field | tenant_id |  | ['"TenantId":"({tenant_id}[^"]+)', '"tenantId"\s*:\s*"({tenant_id}[^"]+)'] |