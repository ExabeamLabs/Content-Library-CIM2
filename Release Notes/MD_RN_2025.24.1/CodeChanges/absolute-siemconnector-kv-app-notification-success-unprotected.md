# Code Changes for absolute-siemconnector-kv-app-notification-success-unprotected (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'email_address', 'event_name', 'host', 'object', 'operation', 'src_host', 'time', 'user'] |
| edit_regex_field | operation |  | ['({event_name}({operation}DeviceBecameAVUnprotected))'] |
| added_regex_field | event_name |  | ['({event_name}({operation}DeviceBecameAVUnprotected))'] |
| removed_attribute | DupFields |  | N/A |