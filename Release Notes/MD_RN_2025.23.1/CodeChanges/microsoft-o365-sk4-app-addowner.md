# Code Changes for microsoft-o365-sk4-app-addowner (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_name', 'additional_info', 'app', 'browser', 'correlation_id', 'dest_domain', 'domain', 'email_address', 'email_domain', 'event_name', 'failure_reason', 'host', 'object', 'operation', 'os', 'resource', 'result', 'src_host', 'src_ip', 'src_port', 'target', 'time', 'user', 'user_agent', 'user_type', 'user_upn'] |
| edit_regex_field | operation |  | ['"Operation\\*"+:[\s\\]*"+({event_name}({operation}[^"\\\.]*))', '\sact=({event_name}({operation}[^=]+?))\s+(\w+=|$)'] |
| added_regex_field | event_name |  | ['"Operation\\*"+:[\s\\]*"+({event_name}({operation}[^"\\\.]*))', '\sact=({event_name}({operation}[^=]+?))\s+(\w+=|$)'] |
| removed_attribute | DupFields |  | N/A |