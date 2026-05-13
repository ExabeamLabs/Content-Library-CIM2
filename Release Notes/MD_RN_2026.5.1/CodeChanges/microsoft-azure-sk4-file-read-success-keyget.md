# Code Changes for microsoft-azure-sk4-file-read-success-keyget (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'email_address', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'http_response_code', 'object', 'operation', 'result', 'src_file_ext', 'src_file_name', 'src_file_path', 'src_ip', 'src_port', 'tenant_id', 'time', 'user'] |
| edit_regex_field | event_name |  | ['"OperationName":\"({operation}({event_name}[^\"]+))"'] |
| edit_regex_field | http_response_code |  | ['httpStatusCode_d":"?({http_response_code}\d+)'] |
| added_regex_field | operation |  | ['"OperationName":\"({operation}({event_name}[^\"]+))"'] |
| added_regex_field | tenant_id |  | ['"TenantId":\s*"({tenant_id}[^"]+)"'] |