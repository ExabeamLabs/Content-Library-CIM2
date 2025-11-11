# Code Changes for microsoft-sysmon-xml-file-time-modify-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'dest_host', 'event_code', 'event_id', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'host', 'log_name', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'result', 'run_level', 'time', 'user_sid'] |
| edit_regex_field | event_name |  | ['({access}({event_name}File creation time changed))'] |
| added_regex_field | access |  | ['({access}({event_name}File creation time changed))'] |
| removed_attribute | DupFields |  | N/A |