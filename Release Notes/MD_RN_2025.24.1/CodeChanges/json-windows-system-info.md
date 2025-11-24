# Code Changes for json-windows-system-info (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['event_code', 'log_source', 'login_id', 'src_port', 'time', 'user_sid'] |
| removed_regex_field | domain |  | [] |
| removed_regex_field | src_domain |  | [] |
| removed_regex_field | src_ip |  | [] |
| edit_regex_field | src_port |  | ['"IpPort":"({src_port}\d{1,5})'] |
| removed_regex_field | src_user |  | [] |
| removed_regex_field | user |  | [] |