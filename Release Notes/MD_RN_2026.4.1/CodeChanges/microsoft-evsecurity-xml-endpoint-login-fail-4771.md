# Code Changes for microsoft-evsecurity-xml-endpoint-login-fail-4771 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'failure_code', 'host', 'result_code', 'run_level', 'src_ip', 'src_port', 'time', 'user', 'user_sid', 'user_upn'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |