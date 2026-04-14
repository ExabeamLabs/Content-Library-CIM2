# Code Changes for pan-tesm-csv-alert-trigger-hipmatch (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action_flags', 'domain', 'email_address', 'event_category', 'event_name', 'firewall', 'hip_type', 'host', 'host_type', 'object', 'os', 'profile', 'repeat_count', 'seq_num', 'serial_num', 'src_host', 'src_ip', 'src_port', 'time', 'user', 'virtual_system'] |
| added_regex_field | event_category |  | [',({event_category}HIPMATCH)'] |