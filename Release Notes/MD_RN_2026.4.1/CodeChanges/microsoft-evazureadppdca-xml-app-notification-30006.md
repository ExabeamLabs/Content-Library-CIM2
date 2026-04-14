# Code Changes for microsoft-evazureadppdca-xml-app-notification-30006 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed | Conditions |  | ['<EventID>30006</EventID>', 'Microsoft-AzureADPasswordProtection-DCAgent'] |
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'event_code', 'event_name', 'host', 'operation', 'process_id', 'result', 'run_level', 'thread_id', 'time', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<\/Channel>'] |