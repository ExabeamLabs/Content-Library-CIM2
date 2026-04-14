# Code Changes for cisco-network-http-session-fail-2 (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'cisco-fp-kv-http-session-policy','cisco-fp-kv-http-session-sfims') and (!exists(event_code) || exists(event_code) && event_code != '430004') and !InList(ToLower(action), 'allow', 'trust') |