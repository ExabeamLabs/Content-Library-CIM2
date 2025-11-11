# Code Changes for windows-events-3 (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['aid', 'd_name', 'd_parent', 'login_id', 'result', 'share_name', 'share_path', 'src_port', 'time'] |
| removed_regex_field | dest_ip |  | [] |
| removed_regex_field | dest_port |  | [] |
| removed_regex_field | domain |  | [] |
| removed_regex_field | full_name |  | [] |
| removed_regex_field | src_ip |  | [] |
| edit_regex_field | src_port |  | ['Source Port(=|:)\s*({src_port}\d+)'] |
| removed_regex_field | user |  | [] |