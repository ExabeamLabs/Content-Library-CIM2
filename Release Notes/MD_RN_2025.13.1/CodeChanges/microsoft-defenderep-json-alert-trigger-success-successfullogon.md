# Code Changes for microsoft-defenderep-json-alert-trigger-success-successfullogon (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'domain', 'email_address', 'email_domain', 'file_dir', 'file_ext', 'file_name', 'full_name', 'incident_status', 'malware_family', 'process_id', 'process_name', 'result', 'src_host', 'src_ip', 'src_port', 'technique', 'time', 'user', 'user_upn'] |
| removed_regex_field | file_path |  | [] |
| added_regex_field | file_dir |  | ['"entityType":\s*"File"[^\}]+?"filePath":\s*"({file_dir}[^"]+)"', 'exa_regex="entityType":\s*"File"[^\}]+?"filePath":\s*"({file_dir}[^"]+)"'] |
| added_regex_field | result |  | ['"evidence".+?"verdict":"({result}[^"]+)', 'exa_regex="evidence".+?"verdict":"({result}[^"]+)"'] |
| added_regex_field | technique |  | ['"mitreTechniques":\[({technique}[^\]]+)\]'] |