# Code Changes for microsoft-defenderep-kv-dll-load-eventhubbeat (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['category', 'dest_host', 'domain', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'hash_md5', 'host', 'login_id', 'process_command_line', 'process_dir', 'process_id', 'process_name', 'process_path', 'tenant_id', 'time', 'user', 'user_sid'] |
| added_regex_field | tenant_id |  | ['"tenantId"\s*:\s*"({tenant_id}[^"]+)"'] |