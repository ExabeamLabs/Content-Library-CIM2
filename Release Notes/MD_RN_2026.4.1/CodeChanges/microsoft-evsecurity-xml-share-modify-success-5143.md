# Code Changes for microsoft-evsecurity-xml-share-modify-success-5143 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'd_name', 'd_parent', 'domain', 'event_code', 'event_name', 'file_type', 'host', 'login_id', 'run_level', 'share_name', 'share_path', 'src_domain', 'src_user', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |