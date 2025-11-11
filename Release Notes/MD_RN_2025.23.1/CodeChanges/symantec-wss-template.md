# Code Changes for symantec-wss-template (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'dest_ip', 'dest_port', 'host', 'time'] |
| added_regex_field | dest_host |  | ['({dest_host}[\w.-]+) ProxySG:'] |
| removed_attribute | DupFields |  | N/A |