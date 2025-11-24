# Code Changes for netapp-json-windows-events-1 (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'access_mask', 'auth_package', 'dest_user_sid', 'event_code', 'event_name', 'file_ext', 'file_name', 'file_path', 'file_type', 'handle_id', 'keywords', 'login_type', 'new_sd', 'object', 'object_class', 'object_server', 'old_sd', 'opcode', 'provider_guid', 'provider_name', 'registry_key', 'registry_path', 'result', 'src_port', 'time', 'user_sid', 'user_uid'] |
| removed_regex_field | dest_domain |  | [] |
| removed_regex_field | dest_user |  | [] |
| removed_regex_field | domain |  | [] |
| removed_regex_field | src_ip |  | [] |
| edit_regex_field | src_port |  | ["'IpPort':\s+({src_port}\d+)"] |
| removed_regex_field | user |  | [] |