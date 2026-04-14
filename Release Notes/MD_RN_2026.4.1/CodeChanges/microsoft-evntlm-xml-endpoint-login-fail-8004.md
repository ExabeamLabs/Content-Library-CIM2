# Code Changes for microsoft-evntlm-xml-endpoint-login-fail-8004 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_host', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'policy_name', 'process_id', 'resource', 'run_level', 'src_host', 'time', 'user', 'user_sid', 'user_upn'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<\/Channel>'] |