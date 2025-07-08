# Code Changes for microsoft-evapp-xml-endpoint-notification-5443 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | event_id | ['<EventRecordID>({event_id}[^<]+)<\/EventRecordID>', '<EventRecordID>({event_id}[^<]+?)<\/EventRecordID>'] | ['<EventRecordID>({event_id}[^<]+?)<\/EventRecordID>'] |