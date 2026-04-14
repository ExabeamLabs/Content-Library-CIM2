# Code Changes for microsoft-evpowershell-kv-process-create-success-executing (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'command', 'command_invocation', 'command_type', 'dest_host', 'domain', 'engine_version', 'event_code', 'event_name', 'host', 'process_command_line', 'process_dir', 'process_id', 'process_name', 'process_path', 'script_name', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<\/Channel>'] |