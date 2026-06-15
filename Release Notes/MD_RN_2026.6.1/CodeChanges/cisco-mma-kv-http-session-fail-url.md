# Code Changes for cisco-mma-kv-http-session-fail-url (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['({time}\d{10})\.\d+\s+({host}[\w.\-]+)\s+events content_filtering_block'] |
| edit_regex_field | time |  | ['({time}\d{10})\.\d+\s+({host}[\w.\-]+)\s+events content_filtering_block'] |