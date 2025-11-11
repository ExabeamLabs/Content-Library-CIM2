# Code Changes for microsoft-evsecurity-sk4-endpoint-4624 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'access_mask', 'auth_package', 'dest_domain', 'dest_host', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'file_ext', 'file_name', 'file_path', 'handle_id', 'host', 'keywords', 'login_type', 'new_sd', 'object', 'object_class', 'object_server', 'old_sd', 'opcode', 'provider_guid', 'provider_name', 'result', 'src_domain', 'src_ip', 'src_port', 'src_user', 'time', 'user', 'user_sid', 'user_uid'] |
| edit_regex_field | host |  | ["'Computer':\s+'({dest_host}({host}[\w\-\.]+))", "'Computer':\s+'({host}[^']+)"] |
| added_regex_field | dest_host |  | ["'Computer':\s+'({dest_host}({host}[\w\-\.]+))"] |
| added_regex_field | domain |  | ["'TargetDomainName':\s+'({domain}[^']+)"] |
| added_regex_field | user |  | ["'TargetUserName':\s+'({user}[\w\.\-\!\#\^\~]{1,40}\$?)"] |
| removed_attribute | DupFields |  | N/A |