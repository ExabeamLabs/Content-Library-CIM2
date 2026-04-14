# Code Changes for microsoft-evapp-xml-endpoint-notification-3005 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'channel', 'dest_host', 'device_name', 'domain', 'event_code', 'event_id', 'failure_reason', 'file_path', 'host', 'process_id', 'process_name', 'src_ip', 'time', 'uri_path', 'url', 'user'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<\/Channel>'] |