# Code Changes for microsoft-o365-sk4-app-file-success-group (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'category', 'connection_id', 'dest_email_address', 'dest_email_domain', 'dest_user', 'email_address', 'email_domain', 'event_name', 'log_source', 'object', 'object_id', 'object_type', 'operation', 'os', 'resource', 'result', 'src_ip', 'src_port', 'time', 'user_agent'] |
| edit_regex_field | object |  | ['"targetResources":[^\}]+?"displayName":"\s*({resource}({object}[^"]+?))\s*"', '\sfname=\s*(N\/A|({resource}({object}[^=]+?)))\s*(\w+=|$)'] |
| added_regex_field | resource |  | ['"targetResources":[^\}]+?"displayName":"\s*({resource}({object}[^"]+?))\s*"', '\sfname=\s*(N\/A|({resource}({object}[^=]+?)))\s*(\w+=|$)'] |
| removed_attribute | DupFields |  | N/A |