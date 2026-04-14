# Code Changes for json-windows-events-2 (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'activity_id', 'app', 'channel', 'event_code', 'event_id', 'event_name', 'key_name', 'key_type', 'login_id', 'login_type', 'operation', 'os', 'privileges', 'process_id', 'provider_name', 'result', 'sid_history', 'task_name', 'thread_id', 'time', 'user_sid'] |
| added_regex_field | channel |  | ['"channel\\?"+:\\?"+({channel}[^"\\]+)'] |