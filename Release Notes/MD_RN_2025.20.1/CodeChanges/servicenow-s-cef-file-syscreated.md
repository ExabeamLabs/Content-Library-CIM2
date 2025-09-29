# Code Changes for servicenow-s-cef-file-syscreated (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'activity_details', 'additional_info', 'app', 'bytes', 'category', 'dproc', 'email_address', 'email_domain', 'event_name', 'file_ext', 'file_name', 'file_type', 'new_value', 'object', 'old_value', 'operation', 'operator_name', 'priority', 'resource', 'severity', 'src_ip', 'src_port', 'status_msg', 'sub_category', 'table', 'table_name', 'time', 'url', 'user'] |
| removed_regex_field | state |  | [] |
| added_regex_field | status_msg |  | ['"state":"({status_msg}[^"]+)"'] |