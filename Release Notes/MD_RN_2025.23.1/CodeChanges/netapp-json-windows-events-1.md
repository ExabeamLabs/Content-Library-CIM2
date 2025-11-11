# Code Changes for netapp-json-windows-events-1 (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'access_mask', 'auth_package', 'dest_domain', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'file_ext', 'file_name', 'file_path', 'file_type', 'handle_id', 'keywords', 'login_type', 'new_sd', 'object', 'object_class', 'object_server', 'old_sd', 'opcode', 'provider_guid', 'provider_name', 'registry_key', 'registry_path', 'result', 'src_ip', 'src_port', 'time', 'user', 'user_sid', 'user_uid'] |
| edit_regex_field | access |  | ["'AccessList':\s+'({event_name}({access}.+?))\s*'", "'EventName':\s+'({event_name}({access}[^']+))"] |
| edit_regex_field | object_class |  | ["'ObjectType':\s+'({file_type}({object_class}[^']+))"] |
| added_regex_field | event_name |  | ["'AccessList':\s+'({event_name}({access}.+?))\s*'", "'EventName':\s+'({event_name}({access}[^']+))"] |
| added_regex_field | file_type |  | ["'ObjectType':\s+'({file_type}({object_class}[^']+))"] |