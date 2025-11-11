# Code Changes for microsoft-evsecurity-xml-policy-apply-6144 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'dest_process_dir', 'dest_process_name', 'dest_process_path', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'policy_content', 'policy_name', 'process_dir', 'process_id', 'process_name', 'process_path', 'result', 'run_level', 'src_ip', 'src_port', 'task_name', 'thread_id', 'time', 'user', 'user_sid'] |
| edit_regex_field | policy_name |  | ['<Data Name=(\'|")GPOList(\'|")>({policy_content}({policy_name}[^<]+))<'] |
| added_regex_field | policy_content |  | ['<Data Name=(\'|")GPOList(\'|")>({policy_content}({policy_name}[^<]+))<'] |
| removed_attribute | DupFields |  | N/A |