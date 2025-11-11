# Code Changes for symantec-wss-str-endpoint-notification-success-lookupfailedforgroup (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'dest_ip', 'dest_port', 'event_code', 'event_name', 'group_domain', 'group_name', 'host', 'severity', 'time'] |
| added_regex_field | dest_host |  | ['({dest_host}[\w.-]+) ProxySG:'] |
| removed_attribute | DupFields |  | N/A |