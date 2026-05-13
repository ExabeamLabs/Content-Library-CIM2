# Code Changes for microsoft-sysmon-xml-file-write-success-13 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_host', 'event_code', 'host', 'operation', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'registry_details', 'registry_details_type', 'registry_key', 'registry_path', 'registry_value', 'result', 'run_level', 'time', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |