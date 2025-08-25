# Code Changes for microsoft-evsystem-xml-process-create-success-5861 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'dest_host', 'event_code', 'host', 'process_command_line', 'process_name', 'run_level', 'time', 'user_sid'] |
| removed_regex_field | process_path |  | [] |
| added_regex_field | additional_info |  | ['Consumer:\s* instance of\s*({additional_info}.+?)\s*\{'] |