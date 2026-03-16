# Code Changes for dell-alert-trigger-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'dell-sw-kv-alert-trigger-success-security') && InList(message_id, '82', '83', '177', '608', '609', '904', '1198', '1199', '1369','1154','1179') && toLower(action)!='drop' |