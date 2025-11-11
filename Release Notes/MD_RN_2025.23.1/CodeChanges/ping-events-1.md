# Code Changes for ping-events-1 (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'auth_type', 'email_address', 'host', 'host_ip', 'protocol', 'result', 'src_ip', 'src_port', 'user'] |
| edit_regex_field | protocol |  | ['(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|SLO|AUTHN_SESSIONS_DELETED)\s*\|)([^\|]*\|)(\s*tid:[^\|]*\|)?([^\|]*\|){3}\s*(|-|({auth_type}({protocol}[^\s\|]+)))\|'] |
| added_regex_field | auth_type |  | ['(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|SLO|AUTHN_SESSIONS_DELETED)\s*\|)([^\|]*\|)(\s*tid:[^\|]*\|)?([^\|]*\|){3}\s*(|-|({auth_type}({protocol}[^\s\|]+)))\|'] |
| removed_attribute | DupFields |  | N/A |