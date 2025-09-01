# Code Changes for servicenow-s-cef-file-syscreated (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'activity_details', 'additional_info', 'app', 'bytes', 'category', 'dproc', 'email_address', 'email_domain', 'event_name', 'file_ext', 'file_name', 'file_type', 'new_value', 'object', 'old_value', 'operation', 'operator_name', 'priority', 'resource', 'severity', 'src_ip', 'src_port', 'state', 'sub_category', 'table', 'table_name', 'time', 'url', 'user'] |
| added_regex_field | activity_details |  | ['"work_notes":"({activity_details}[^"]+)"'] |
| added_regex_field | category |  | ['"category":"({category}[^"]+)"'] |
| added_regex_field | operator_name |  | ['"sys_updated_by":"({operator_name}[^"]+)"'] |
| added_regex_field | state |  | ['"state":"({state}[^"]+)"'] |
| added_regex_field | sub_category |  | ['"subcategory":"({sub_category}[^"]+)"'] |