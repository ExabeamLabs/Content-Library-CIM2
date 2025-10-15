# Code Changes for fortinet-fortisiem-kv-email-statistics (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'category', 'dest_email_address', 'dest_email_domain', 'dest_host', 'dest_ip', 'dest_port', 'device_id', 'direction', 'email_address', 'email_domain', 'email_subject', 'event_category', 'event_name', 'host', 'session_id', 'severity', 'src_host', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | host |  | ['\Wdevname="({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | dest_host |  | ['\Wdevname="({dest_host}({host}[\w\-.]+))'] |
| removed_attribute | DupFields |  | N/A |