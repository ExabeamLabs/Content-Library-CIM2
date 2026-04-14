# Code Changes for microsoft-evsecurity-xml-endpoint-login-4776 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_domain', 'dest_user', 'domain', 'error_code', 'event_code', 'event_name', 'failure_code', 'host', 'login_type_text', 'result', 'result_code', 'run_level', 'src_host', 'src_ip', 'src_port', 'time', 'user', 'user_upn'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |