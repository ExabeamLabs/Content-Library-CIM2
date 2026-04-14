# Code Changes for microsoft-evsecurity-sk4-peripheral_storage-insert-success-6416 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'device_pid', 'device_vid', 'domain', 'event_code', 'event_name', 'host', 'log_source', 'login_id', 'src_domain', 'src_ip', 'src_port', 'src_user', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)', 'Channel"?(:|=)"?({channel}[^"<]+)'] |