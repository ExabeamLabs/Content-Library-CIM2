# Code Changes for microsoft-evterminalserviceslicensing-xml-endpoint-notification-success-4105 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'dest_process_dir', 'dest_process_name', 'dest_process_path', 'domain', 'error_code', 'event_code', 'event_id', 'event_name', 'failure_code', 'host', 'login_id', 'process_dir', 'process_id', 'process_name', 'process_path', 'provider_name', 'result', 'run_level', 'src_ip', 'src_port', 'task_name', 'thread_id', 'time', 'user', 'user_sid'] |
| edit_regex_field | error_code |  | ['<param3>({failure_code}({error_code}[^<]+))<'] |
| added_regex_field | failure_code |  | ['<param3>({failure_code}({error_code}[^<]+))<'] |
| removed_attribute | DupFields |  | N/A |