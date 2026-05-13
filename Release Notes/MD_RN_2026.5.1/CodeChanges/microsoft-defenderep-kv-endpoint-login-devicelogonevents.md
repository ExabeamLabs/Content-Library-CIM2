# Code Changes for microsoft-defenderep-kv-endpoint-login-devicelogonevents (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['category', 'dest_host', 'domain', 'event_name', 'file_name', 'file_path', 'hash_md5', 'host', 'login_id', 'login_type', 'parent_process_name', 'process_command_line', 'process_dir', 'process_id', 'process_integrity', 'process_name', 'tenant_id', 'time', 'user', 'user_sid'] |
| added_regex_field | tenant_id |  | ['"tenantId"\s*:\s*"({tenant_id}[^"]+)"'] |