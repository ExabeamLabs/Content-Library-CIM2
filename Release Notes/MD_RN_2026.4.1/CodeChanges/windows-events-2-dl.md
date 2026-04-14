# Code Changes for windows-events-2-dl (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'event_code', 'event_id', 'operation', 'provider_name'] |
| added_regex_field | channel |  | ['\schannel="+({channel}[^"]+)"'] |