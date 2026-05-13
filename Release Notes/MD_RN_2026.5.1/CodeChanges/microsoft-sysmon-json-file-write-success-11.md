# Code Changes for microsoft-sysmon-json-file-write-success-11 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'creation_utc_time', 'domain', 'event_code', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'host', 'process_dir', 'process_id', 'process_name', 'process_path', 'time', 'user'] |
| added_regex_field | channel |  | ['"Channel"+:"+({channel}[^"]+)"'] |