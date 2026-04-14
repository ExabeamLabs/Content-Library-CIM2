# Code Changes for microsoft-evapp-xml-policy-apply-fail-4098 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'error_code', 'event_code', 'event_id', 'event_name', 'host', 'result', 'run_level', 'time', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<\/Channel>'] |