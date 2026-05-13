# Code Changes for microsoft-evsystem-xml-process-create-success-5861 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'dest_host', 'event_code', 'host', 'process_command_line', 'process_name', 'run_level', 'time', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |