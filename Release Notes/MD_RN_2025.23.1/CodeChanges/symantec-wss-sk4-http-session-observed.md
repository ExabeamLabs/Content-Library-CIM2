# Code Changes for symantec-wss-sk4-http-session-observed (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'category', 'dest_ip', 'dest_port', 'host', 'http_response_code', 'method', 'mime', 'process_name', 'protocol', 'proxy_action', 'referrer', 'result_code', 'src_host', 'src_ip', 'src_port', 'time', 'transaction_id', 'uri_path', 'uri_query', 'url', 'user', 'user_agent'] |
| added_regex_field | http_response_code |  | [',\sOBSERVED(,\s([^,]+)){2},\s(-|({http_response_code}\d{1,3}))'] |
| removed_attribute | DupFields |  | N/A |