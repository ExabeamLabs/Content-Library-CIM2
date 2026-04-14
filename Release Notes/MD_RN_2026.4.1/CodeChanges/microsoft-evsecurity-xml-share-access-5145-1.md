# Code Changes for microsoft-evsecurity-xml-share-access-5145-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'd_name', 'd_parent', 'domain', 'event_code', 'event_id', 'file_dir', 'file_ext', 'file_name', 'file_type', 'host', 'login_id', 'run_level', 'share_name', 'share_path', 'src_domain', 'src_ip', 'src_port', 'src_user', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |