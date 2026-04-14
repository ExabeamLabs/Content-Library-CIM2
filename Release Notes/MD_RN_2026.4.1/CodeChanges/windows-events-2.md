# Code Changes for windows-events-2 (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'event_code', 'login_id', 'login_type', 'process_dir', 'process_id', 'process_name', 'process_path', 'provider_name', 'src_port', 'time', 'user_sid'] |
| added_regex_field | channel |  | ['channel="({channel}[^"]+)'] |