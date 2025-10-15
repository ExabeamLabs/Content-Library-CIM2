# Code Changes for s-xml-windows-member (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'account_name', 'additional_info', 'channel', 'dest_ip', 'dest_port', 'dest_user_sid', 'domain', 'event_code', 'event_id', 'event_name', 'group_domain', 'group_id', 'group_name', 'login_id', 'member', 'opcode', 'process_guid', 'process_id', 'provider_name', 'result', 'run_level', 'src_ip', 'src_port', 'task_name', 'time', 'user', 'user_dn', 'user_ou', 'user_sid'] |
| edit_regex_field | group_name |  | ['<Data Name(\\)?=(\'|")TargetUserName(\'|")>(?=\w)?({group_name}[^<]+)</Data>'] |
| edit_regex_field | process_guid |  | ['<System>.*?Guid(\\)?=(\'|")\{({process_guid}[^}]+)', 'Guid\\*=(\'|")\{({process_guid}[^\\'\}]+)'] |
| edit_regex_field | provider_name |  | ['<Provider>({provider_name}[^<]+)', 'Provider Name\\*=(\'|")({provider_name}[^\\'"]+)'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |
| added_regex_field | event_id |  | ['<EventRecordID>({event_id}[^<]+)<'] |
| added_regex_field | opcode |  | ['<Opcode>({opcode}[^<]+?)<'] |
| added_regex_field | result |  | ['<Keywords>({result}[^<]+)<'] |
| added_regex_field | task_name |  | ['<Task>({task_name}[^<]+)<'] |