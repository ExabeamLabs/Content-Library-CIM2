# Code Changes for zscaler-ia-json-http-session-transactionsize (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'app', 'bytes', 'bytes_in', 'bytes_out', 'category', 'department', 'dest_ip', 'email_address', 'failure_reason', 'http_response_code', 'location', 'method', 'protocol', 'referrer', 'result_code', 'src_host', 'src_ip', 'time', 'uri_path', 'uri_query', 'url', 'user', 'user_agent', 'web_domain'] |
| added_regex_field | http_response_code |  | ['"status":"({http_response_code}\d{1,3})"'] |
| removed_attribute | DupFields |  | N/A |