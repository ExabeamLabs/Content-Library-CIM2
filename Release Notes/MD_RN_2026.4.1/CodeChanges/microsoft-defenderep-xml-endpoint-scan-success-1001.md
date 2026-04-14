# Code Changes for microsoft-defenderep-xml-endpoint-scan-success-1001 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'event_code', 'host', 'provider_guid', 'result', 'run_level', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<\/Channel>'] |