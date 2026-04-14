# Code Changes for hornet-microsoft365-email-receive-success-1 (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type , 'hornet-email-kv-email-receive-success-2') && (exists(result) && InList(result,'8','2') && exists(direction) &&  direction = '1') |