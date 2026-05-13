# Code Changes for microsoft-defenderep-sk4-registry-modify-advancedhunting (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'dest_host', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'host', 'old_registry_details', 'operation', 'operation_type', 'parent_process_name', 'process_command_line', 'process_dir', 'process_id', 'process_name', 'process_path', 'registry_details', 'registry_details_type', 'registry_key', 'registry_path', 'registry_value', 'tenant_id', 'time', 'user', 'user_sid'] |
| edit_regex_field | user |  | ['InitiatingProcessAccountName"+:\s*"+(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|Système|system|local service|({user}[\w\.\-\!\#\^\~]{1,40}\$?))', 'exa_json_path=$..InitiatingProcessAccountName,exa_regex=(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|Système|system|local service|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| added_regex_field | tenant_id |  | ['"tenantId"\s*:\s*"({tenant_id}[^"]+)"'] |