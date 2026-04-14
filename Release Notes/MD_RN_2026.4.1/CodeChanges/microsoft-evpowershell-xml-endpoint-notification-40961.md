# Code Changes for microsoft-evpowershell-xml-endpoint-notification-40961 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'event_code', 'host', 'process_id', 'run_level', 'time'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<\/Channel>'] |