# Code Changes for microsoft-sysmon-xml-registry-rename-success-14 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'domain', 'event_category', 'event_code', 'event_name', 'host', 'old_registry_details', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'provider_name', 'registry_details', 'rule', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |