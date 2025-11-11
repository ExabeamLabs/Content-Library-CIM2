# Code Changes for microsoft-o365-sk4-app-file-success-groupadd (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'category', 'connection_id', 'email_address', 'email_domain', 'event_name', 'file_name', 'group_name', 'log_source', 'object', 'object_id', 'object_type', 'operation', 'os', 'process_name', 'resource', 'result', 'src_ip', 'src_port', 'time', 'user_agent'] |
| edit_regex_field | object |  | ['\sfname=\s*(N\/A|({resource}({object}[^=]+?)))\s*(\w+=|$)'] |
| added_regex_field | resource |  | ['\sfname=\s*(N\/A|({resource}({object}[^=]+?)))\s*(\w+=|$)'] |
| removed_attribute | DupFields |  | N/A |