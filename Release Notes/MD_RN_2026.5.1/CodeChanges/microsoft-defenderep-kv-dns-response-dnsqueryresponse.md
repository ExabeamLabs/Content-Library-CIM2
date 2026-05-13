# Code Changes for microsoft-defenderep-kv-dns-response-dnsqueryresponse (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['category', 'dest_host', 'dns_query', 'domain', 'event_name', 'file_name', 'file_path', 'hash_md5', 'host', 'login_id', 'parent_process_name', 'process_command_line', 'process_dir', 'process_id', 'process_integrity', 'process_name', 'tenant_id', 'time', 'user', 'user_sid'] |
| added_regex_field | tenant_id |  | ['"tenantId"\s*:\s*"({tenant_id}[^"]+)"'] |