# Code Changes for microsoft-o365-json-file-success-workload (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'app', 'file_dir', 'file_name', 'file_type', 'object', 'operation', 'src_file_ext', 'src_ip', 'src_port', 'time', 'user_agent'] |
| edit_regex_field | file_name |  | [',SourceFileName":"({object}({file_name}[^,]+))'] |
| edit_regex_field | operation |  | [',Operation":"({access}({operation}[^,]+))'] |
| added_regex_field | access |  | [',Operation":"({access}({operation}[^,]+))'] |
| added_regex_field | object |  | [',SourceFileName":"({object}({file_name}[^,]+))'] |
| removed_attribute | DupFields |  | N/A |