# Code Changes for microsoft-azuremon-json-app-activity-administrative (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | tenant_id |  | ['"tenantId"\s*:\s*"({tenant_id}[^",]+)', '"tenantId"\s*:\s*"({tenant_id}[^"]+)', 'exa_regex="tenantId"\s*:\s*"({tenant_id}[^",]+)'] |