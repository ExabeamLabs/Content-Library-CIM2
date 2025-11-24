# Code Changes for servicenow-s-cef-file-syscreated (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'action', 'activity_details', 'additional_info', 'app', 'bytes', 'category', 'description', 'dproc', 'email_address', 'email_domain', 'event_name', 'file_ext', 'file_name', 'file_type', 'new_value', 'object', 'old_value', 'operation', 'operator_name', 'priority', 'resource', 'severity', 'src_ip', 'src_port', 'status_msg', 'sub_category', 'table', 'table_name', 'task_id', 'time', 'url', 'user'] |
| edit_regex_field | file_ext |  | ['"file_name"+:"+({object}({file_name}[^"]+?(\.({file_ext}[^\."]+))?))"+,'] |
| edit_regex_field | file_name |  | ['"file_name"+:"+({object}({file_name}[^"]+?(\.({file_ext}[^\."]+))?))"+,'] |
| edit_regex_field | object |  | ['"(instance|documentkey)"+:"+({object}[^"]+?)"+,', '"file_name"+:"+({object}({file_name}[^"]+?(\.({file_ext}[^\."]+))?))"+,'] |
| edit_regex_field | operation |  | ['"queue"+:"+({access}({operation}[^",]+))'] |
| added_regex_field | access |  | ['"queue"+:"+({access}({operation}[^",]+))'] |
| removed_attribute | DupFields |  | N/A |