# Code Changes for microsoft-evpowershell-xml-script-execute-fail-4100 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_severity', 'channel', 'command', 'command_type', 'domain', 'engine_version', 'failure_reason', 'host', 'process_dir', 'process_name', 'process_path', 'run_level', 'script_name', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<\/Channel>'] |