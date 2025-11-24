# Code Changes for unix-auditbeat-kv-endpoint-login-success-userlogin (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'dest_host', 'domain', 'event_name', 'host', 'result', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | host |  | ['"hostname":"({dest_host}({host}[\w\-.]+?))(@[^"]*)?"'] |
| added_regex_field | dest_host |  | ['"hostname":"({dest_host}({host}[\w\-.]+?))(@[^"]*)?"'] |
| removed_attribute | DupFields |  | N/A |