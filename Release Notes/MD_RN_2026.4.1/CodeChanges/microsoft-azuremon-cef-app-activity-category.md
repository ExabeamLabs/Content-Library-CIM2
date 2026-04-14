# Code Changes for microsoft-azuremon-cef-app-activity-category (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | tenant_id |  | ['"tenantId"\s*:\s*"({tenant_id}[^",]+)', '"tenantId"\s*:\s*"({tenant_id}[^"]+)', 'exa_regex="tenantId"\s*:\s*"({tenant_id}[^",]+)'] |
| changed | Conditions |  | ['"category":', '"operationName":', 'CEF:', 'cat=audit ', 'destinationServiceName=Azure'] |