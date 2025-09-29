# Code Changes for f5-asm-kv-alert-trigger-success-botdefense (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'dest_ip', 'dest_port', 'device_ip', 'host', 'method', 'protocol', 'referrer', 'request_cookie', 'server_name', 'session_id', 'src_country_code', 'src_ip', 'src_port', 'status_msg', 'time', 'url', 'user_agent', 'version', 'web_domain'] |
| removed_regex_field | state |  | [] |
| added_regex_field | status_msg |  | [',request_status="({status_msg}[^"]+)'] |