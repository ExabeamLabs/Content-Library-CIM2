# Code Changes for symantec-critical-sys-protection (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'dest_ip', 'dest_port', 'domain', 'event_code', 'host', 'login_type_text', 'parent_process_name', 'policy_name', 'process_name', 'rule', 'session_id', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | dest_host |  | ['\sHOSTNAME\s*:\s*"*({dest_host}[^\s"]+)'] |
| removed_attribute | DupFields |  | N/A |