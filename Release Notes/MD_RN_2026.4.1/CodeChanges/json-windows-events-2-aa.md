# Code Changes for json-windows-events-2-aa (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'auth_process', 'channel', 'event_code', 'login_id', 'process_dir', 'process_id', 'process_name', 'process_path', 'result_code', 'time', 'user_sid'] |
| added_regex_field | channel |  | ['channel\\?"+:\\?"+({channel}[^"\\]+)'] |