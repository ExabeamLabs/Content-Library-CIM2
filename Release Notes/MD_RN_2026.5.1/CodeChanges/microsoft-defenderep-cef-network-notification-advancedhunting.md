# Code Changes for microsoft-defenderep-cef-network-notification-advancedhunting (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | tenant_id |  | ['"tenantId":"({tenant_id}[^",]+)', '"tenantId"\s*:\s*"({tenant_id}[^"]+)"'] |