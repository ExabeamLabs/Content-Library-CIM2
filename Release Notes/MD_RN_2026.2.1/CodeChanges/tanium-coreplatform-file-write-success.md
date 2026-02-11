# Code Changes for tanium-coreplatform-file-write-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'tanium-im-kv-file-write-success-write') && InList(toLower(event_name), 'write') |