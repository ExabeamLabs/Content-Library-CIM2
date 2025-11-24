# Code Changes for wazuh-ssh-login (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['agent_id', 'agent_name', 'decoder_name', 'description', 'dest_host', 'dest_ip', 'dest_user', 'event_code', 'host', 'log_location', 'log_path', 'login_id', 'process_name', 'rule_id', 'src_ip', 'src_port', 'time', 'user', 'wazuh_manager'] |
| edit_regex_field | decoder_name |  | ['"decoder.name":"({process_name}({decoder_name}[^"]+))'] |
| edit_regex_field | dest_user |  | ['"data.dstuser":"(\(no user\)|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| added_regex_field | process_name |  | ['"decoder.name":"({process_name}({decoder_name}[^"]+))'] |
| added_regex_field | user |  | ['"data.dstuser":"(\(no user\)|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| removed_attribute | DupFields |  | N/A |