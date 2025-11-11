# Code Changes for microsoft-o365-sk4-file-write-success-fileuploaded (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'auth_type', 'browser', 'category', 'connection_id', 'email_address', 'email_domain', 'file_name', 'log_source', 'object', 'object_id', 'object_type', 'operation', 'resource', 'result', 'src_file_dir', 'src_ip', 'src_port', 'time', 'user_type'] |
| edit_regex_field | object |  | ['"ObjectId":\s*"({resource}({object}[^"]+))'] |
| added_regex_field | resource |  | ['"ObjectId":\s*"({resource}({object}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |