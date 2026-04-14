# Code Changes for microsoft-evazureadppdca-xml-user-password-reset-fail-30027 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_user', 'event_code', 'event_name', 'full_name', 'host', 'result', 'run_level', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<\/Channel>'] |