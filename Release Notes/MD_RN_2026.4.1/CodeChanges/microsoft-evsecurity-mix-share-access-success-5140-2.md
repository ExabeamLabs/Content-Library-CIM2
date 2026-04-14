# Code Changes for microsoft-evsecurity-mix-share-access-success-5140-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'channel', 'd_name', 'd_parent', 'dest_host', 'dest_ip', 'domain', 'event_code', 'event_name', 'file_path', 'file_type', 'host', 'login_id', 'share_name', 'share_path', 'src_domain', 'src_ip', 'src_port', 'src_user', 'time', 'user'] |
| added_regex_field | channel |  | ['\schannel="+({channel}[^"]+)'] |