# Code Changes for microsoft-evpowershell-kv-script-execute-success-4104 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_host', 'dest_ip', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'operation', 'process_id', 'process_name', 'provider_name', 'scriptblock_id', 'scriptblock_text', 'severity', 'src_ip', 'src_port', 'time', 'user', 'user_upn'] |
| added_regex_field | channel |  | ['channel="({channel}[^"]+)'] |