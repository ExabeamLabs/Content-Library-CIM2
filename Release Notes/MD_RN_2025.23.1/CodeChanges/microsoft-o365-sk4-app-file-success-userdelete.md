# Code Changes for microsoft-o365-sk4-app-file-success-userdelete (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'category', 'connection_id', 'email_address', 'email_domain', 'event_name', 'log_source', 'object', 'object_id', 'object_type', 'operation', 'os', 'resource', 'result', 'src_ip', 'src_port', 'time', 'user_agent'] |
| edit_regex_field | object |  | ['modifiedProperties"+:\[\{[^\}]+\},\{[^\}]+?"+newValue"+:"+\\*"+({resource}({object}[^\\"]+))'] |
| added_regex_field | resource |  | ['modifiedProperties"+:\[\{[^\}]+\},\{[^\}]+?"+newValue"+:"+\\*"+({resource}({object}[^\\"]+))'] |
| removed_attribute | DupFields |  | N/A |