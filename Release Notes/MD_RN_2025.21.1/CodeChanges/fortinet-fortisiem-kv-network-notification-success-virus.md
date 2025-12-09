# Code Changes for fortinet-fortisiem-kv-network-notification-success-virus (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['category', 'dest_email_address', 'dest_email_domain', 'dest_host', 'dest_ip', 'dest_port', 'device_id', 'email_address', 'email_domain', 'event_category', 'event_name', 'failure_reason', 'host', 'operation', 'result', 'session_id', 'severity', 'src_host', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | host |  | ['\Wdevname="({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | dest_host |  | ['\Wdevname="({dest_host}({host}[\w\-.]+))'] |
| removed_attribute | DupFields |  | N/A |