# Code Changes for microsoft-json-events (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'event_name', 'login_id', 'user_sid'] |
| edit_regex_field | domain |  | ['exa_regex=Account Domain:\s+({domain}[^\s]+)'] |
| removed_regex_field | user |  | [] |
| edit_regex_field | user_sid |  | ['exa_regex=Subject:\s+Security ID:\s+({user_sid}[^\s]+)'] |