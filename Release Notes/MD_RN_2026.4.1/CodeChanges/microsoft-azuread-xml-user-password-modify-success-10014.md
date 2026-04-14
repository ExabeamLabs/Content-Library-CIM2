# Code Changes for microsoft-azuread-xml-user-password-modify-success-10014 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed | Conditions |  | ['<EventID>10014</EventID>', 'Microsoft-AzureADPasswordProtection-DCAgent'] |
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'event_code', 'event_name', 'full_name', 'host', 'result', 'run_level', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<\/Channel>'] |