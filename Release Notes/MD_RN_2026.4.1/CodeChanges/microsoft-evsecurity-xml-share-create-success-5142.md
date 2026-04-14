# Code Changes for microsoft-evsecurity-xml-share-create-success-5142 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_host', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'result', 'run_level', 'share_name', 'share_path', 'src_domain', 'src_user', 'time', 'user'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |