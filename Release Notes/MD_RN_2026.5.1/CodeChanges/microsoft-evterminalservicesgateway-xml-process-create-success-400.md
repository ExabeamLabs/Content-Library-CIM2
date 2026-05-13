# Code Changes for microsoft-evterminalservicesgateway-xml-process-create-success-400 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_host', 'event_code', 'event_id', 'event_name', 'host', 'process_command_line', 'process_dir', 'process_name', 'process_path', 'result', 'run_level', 'time'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |