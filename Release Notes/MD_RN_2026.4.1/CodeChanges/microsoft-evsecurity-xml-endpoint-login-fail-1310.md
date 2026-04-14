# Code Changes for microsoft-evsecurity-xml-endpoint-login-fail-1310 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_host', 'domain', 'event_code', 'event_id', 'event_name', 'failure_code', 'failure_reason', 'host', 'provider_name', 'result', 'result_code', 'run_level', 'time', 'user'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |