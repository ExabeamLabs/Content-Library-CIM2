# Code Changes for microsoft-evsystem-xml-endpoint-login-fail-5805 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'domain', 'event_code', 'event_name', 'failure_reason', 'host', 'login_id', 'process_id', 'result', 'run_level', 'severity', 'src_domain', 'src_host', 'src_user', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |