# Code Changes for microsoft-azuremon-sk4-app-activity-operationname (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | tenant_id |  | ['"tenantId"\s*:\s*"({tenant_id}[^",]+)', '"tenantId"\s*:\s*"({tenant_id}[^"]+)', 'exa_regex="tenantId"\s*:\s*"({tenant_id}[^",]+)'] |
| changed | Conditions |  | ['"Category":"', '"OperationName":"', 'CEF:', 'cat=audit ', 'destinationServiceName=Azure'] |