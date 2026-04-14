# Code Changes for microsoft-evsecurity-mix-share-access-5145 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'channel', 'd_name', 'd_parent', 'dest_host', 'dest_ip', 'domain', 'event_code', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_type', 'host', 'log_name', 'login_id', 'result', 'share_name', 'share_path', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | channel |  | ['\schannel="+({channel}[^"]+)'] |