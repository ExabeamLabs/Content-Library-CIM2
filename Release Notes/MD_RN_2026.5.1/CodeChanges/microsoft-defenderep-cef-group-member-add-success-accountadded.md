# Code Changes for microsoft-defenderep-cef-group-member-add-success-accountadded (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'category', 'dest_host', 'dest_ip', 'dest_port', 'event_name', 'group_domain', 'group_name', 'login_id', 'operation', 'process_dir', 'process_integrity', 'process_name', 'process_path', 'protocol', 'src_ip', 'src_port', 'tenant_id', 'time', 'user', 'user_sid'] |
| added_regex_field | tenant_id |  | ['"tenantId":\s*"({tenant_id}[^"]+)"'] |