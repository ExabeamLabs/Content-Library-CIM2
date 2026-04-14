# Code Changes for xml-windows-defender-av (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'event_code', 'provider_guid', 'result', 'run_level', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<\/Channel>'] |