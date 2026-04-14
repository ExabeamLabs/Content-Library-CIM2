# Code Changes for microsoft-evpowershell-xml-process-create-success-4103-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'command_invocation', 'command_module', 'dest_host', 'domain', 'event_code', 'process_command_line', 'process_dir', 'process_name', 'process_path', 'run_level', 'script_name', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |