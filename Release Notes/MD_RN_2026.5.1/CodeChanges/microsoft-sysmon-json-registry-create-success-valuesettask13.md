# Code Changes for microsoft-sysmon-json-registry-create-success-valuesettask13 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'channel', 'dest_host', 'domain', 'event_code', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'host', 'log_name', 'object', 'operation', 'process_guid', 'process_id', 'process_name', 'process_path', 'registry_key', 'registry_path', 'registry_value', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['"Channel"+:"+({channel}[^"]+)"'] |