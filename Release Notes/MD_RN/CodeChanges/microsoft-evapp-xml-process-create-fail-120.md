# Code Changes for microsoft-evapp-xml-process-create-fail-120 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | event_id | ['<EventRecordID>({event_id}[^<]+)<\/EventRecordID>', '<EventRecordID>({event_id}[^<]+?)<\/EventRecordID>'] | ['<EventRecordID>({event_id}[^<]+?)<\/EventRecordID>'] |