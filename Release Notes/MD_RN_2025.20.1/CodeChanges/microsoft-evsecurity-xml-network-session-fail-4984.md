# Code Changes for microsoft-evsecurity-xml-network-session-fail-4984 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'dest_ip', 'dest_port', 'event_code', 'failure_reason', 'host', 'process_id', 'role', 'run_level', 'service_state', 'src_ip', 'src_port', 'task_name', 'time'] |
| removed_regex_field | state |  | [] |
| added_regex_field | service_state |  | ['<Data Name\\*=(\'|")State(\'|")>({service_state}[^<]+)'] |