# Code Changes for microsoft-defenderep-sk4-alert-trigger-acgenforced (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | tenant_id |  | ['"tenantId":"({tenant_id}[^",]+)', '"tenantId"\s*:\s*"({tenant_id}[^"]+)"'] |