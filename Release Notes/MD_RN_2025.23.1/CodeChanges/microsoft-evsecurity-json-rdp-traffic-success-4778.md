# Code Changes for microsoft-evsecurity-json-rdp-traffic-success-4778 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | host |  | ['"Hostname\\?":\\?"({dest_host}({host}[\w.-]+?))\\?"'] |
| added_regex_field | dest_host |  | ['"Hostname\\?":\\?"({dest_host}({host}[\w.-]+?))\\?"'] |
| removed_attribute | DupFields |  | N/A |