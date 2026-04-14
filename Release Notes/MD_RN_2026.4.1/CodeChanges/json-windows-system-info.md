# Code Changes for json-windows-system-info (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'event_code', 'log_source', 'login_id', 'src_port', 'time', 'user_sid'] |
| added_regex_field | channel |  | ['Channel":"({channel}[^"]+)'] |