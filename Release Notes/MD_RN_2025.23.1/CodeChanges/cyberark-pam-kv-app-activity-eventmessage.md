# Code Changes for cyberark-pam-kv-app-activity-eventmessage (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'account', 'app', 'app_type', 'dest_host', 'domain', 'event_code', 'host', 'object', 'operation', 'process_name', 'protocol', 'session_id', 'severity', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | access |  | ['EventMessage="?({access}[^"=,]+)'] |
| removed_attribute | DupFields |  | N/A |