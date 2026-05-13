# Code Changes for microsoft-evsystem-xml-endpoint-login-fail-5805-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'event_code', 'event_name', 'failure_reason', 'host', 'run_level', 'src_host', 'time'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |