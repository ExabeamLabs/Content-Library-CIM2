# Code Changes for microsoft-evsystem-xml-endpoint-notification-1000 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | event_id | ['<EventRecordID>({event_id}[^<]+)<\/EventRecordID>', '<EventRecordID>({event_id}[^<]+?)<\/EventRecordID>'] | ['<EventRecordID>({event_id}[^<]+?)<\/EventRecordID>'] |