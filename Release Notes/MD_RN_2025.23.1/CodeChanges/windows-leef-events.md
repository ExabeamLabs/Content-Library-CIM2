# Code Changes for windows-leef-events (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'attribute', 'domain', 'event_code', 'event_name', 'group_domain', 'group_name', 'login_id', 'result', 'severity', 'time'] |
| removed_regex_field | dest_host |  | [] |
| edit_regex_field | domain |  | ['Account Domain:\s+({domain}[^:]+?)\s+Logon ID:'] |
| removed_regex_field | user |  | [] |