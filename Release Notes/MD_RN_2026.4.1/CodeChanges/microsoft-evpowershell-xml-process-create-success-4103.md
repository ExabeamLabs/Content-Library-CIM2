# Code Changes for microsoft-evpowershell-xml-process-create-success-4103 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'command', 'command_invocation', 'command_module', 'command_type', 'dest_host', 'domain', 'engine_version', 'event_code', 'host', 'powershell_image', 'process_command_line', 'process_dir', 'process_id', 'process_name', 'process_path', 'run_level', 'script_name', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<\/Channel>'] |