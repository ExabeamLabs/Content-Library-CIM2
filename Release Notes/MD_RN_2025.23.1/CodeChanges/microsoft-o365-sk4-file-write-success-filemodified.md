# Code Changes for microsoft-o365-sk4-file-write-success-filemodified (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'auth_type', 'browser', 'bytes', 'category', 'connection_id', 'email_address', 'email_domain', 'log_source', 'object', 'object_id', 'object_type', 'operation', 'os', 'resource', 'result', 'src_file_dir', 'src_file_ext', 'src_file_name', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | object |  | ['"ObjectId":\s*"({resource}({object}[^"]+))', 'exa_regex="ObjectId":\s*"({resource}({object}[^"]+))'] |
| added_regex_field | resource |  | ['"ObjectId":\s*"({resource}({object}[^"]+))', 'exa_regex="ObjectId":\s*"({resource}({object}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |