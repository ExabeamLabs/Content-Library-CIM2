# Code Changes for microsoft-evdnsserver-xml-process-create-success-800-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'command_invocation', 'command_module', 'domain', 'event_code', 'host', 'powershell_image', 'process_command_line', 'process_dir', 'process_name', 'process_path', 'run_level', 'time', 'user'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |