# Code Changes for microsoft-evsecurity-xml-endpoint-time-modify-4616-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'domain', 'event_code', 'event_id', 'host', 'login_id', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'provider_name', 'result', 'run_level', 'src_domain', 'src_user', 'sub_category', 'thread_id', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |