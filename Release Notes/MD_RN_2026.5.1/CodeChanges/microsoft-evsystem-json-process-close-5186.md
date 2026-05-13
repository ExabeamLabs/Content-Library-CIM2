# Code Changes for microsoft-evsystem-json-process-close-5186 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'event_category', 'event_code', 'event_id', 'event_name', 'host', 'process_id', 'severity', 'time'] |
| added_regex_field | channel |  | ['"Channel"+:"+({channel}[^"]+)"'] |