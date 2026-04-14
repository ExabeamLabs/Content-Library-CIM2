# Code Changes for microsoft-evsecurity-str-registry-create-success-4657 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'domain', 'event_code', 'event_name', 'handle_id', 'host', 'login_id', 'old_registry_details', 'old_registry_details_type', 'operation', 'process_dir', 'process_id', 'process_name', 'process_path', 'registry_details', 'registry_details_type', 'registry_key', 'registry_path', 'registry_value', 'result', 'src_host', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['"channel":"({channel}[^"]+)"', '<Channel>({channel}[^<]+)<', 'Channel="({channel}[^"]+)'] |