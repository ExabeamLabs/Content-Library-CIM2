# Code Changes for sophos-ep-cef-app-notification-registered (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'dest_host', 'domain', 'event_category', 'event_name', 'first_name', 'full_name', 'host', 'last_name', 'severity', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | host |  | ['"location":"({src_host}({host}[\w\-.]+))"'] |
| added_regex_field | src_host |  | ['"location":"({src_host}({host}[\w\-.]+))"'] |
| removed_attribute | DupFields |  | N/A |