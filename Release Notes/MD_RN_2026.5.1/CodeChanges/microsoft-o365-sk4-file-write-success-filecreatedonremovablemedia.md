# Code Changes for microsoft-o365-sk4-file-write-success-filecreatedonremovablemedia (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['bytes', 'dest_host', 'device_id', 'device_type', 'domain', 'email_address', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'first_name', 'full_name', 'hash_sha1', 'hash_sha256', 'host', 'last_name', 'operation', 'process_name', 'src_file_ext', 'src_file_name', 'src_ip', 'src_port', 'tenant_id', 'time', 'user', 'user_sid'] |
| added_regex_field | tenant_id |  | ['"(?i:tenantid)":"?({tenant_id}[^"]+),'] |