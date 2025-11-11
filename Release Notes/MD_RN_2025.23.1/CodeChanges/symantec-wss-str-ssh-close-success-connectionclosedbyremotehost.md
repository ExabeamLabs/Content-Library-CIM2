# Code Changes for symantec-wss-str-ssh-close-success-connectionclosedbyremotehost (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'dest_ip', 'dest_port', 'event_category', 'event_code', 'event_name', 'host', 'severity', 'time'] |
| added_regex_field | dest_host |  | ['({dest_host}[\w.-]+) ProxySG:'] |
| removed_attribute | DupFields |  | N/A |