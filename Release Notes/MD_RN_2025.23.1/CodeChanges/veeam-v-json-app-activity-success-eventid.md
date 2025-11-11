# Code Changes for veeam-v-json-app-activity-success-eventid (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'channel', 'event_id', 'host', 'opcode', 'process_id', 'resource_name', 'severity', 'thread_id', 'time'] |
| added_regex_field | additional_info |  | ['"Message":"({additional_info}[^"]+)"'] |