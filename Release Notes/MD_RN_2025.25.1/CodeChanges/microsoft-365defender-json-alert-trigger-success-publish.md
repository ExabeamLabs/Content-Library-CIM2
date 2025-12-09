# Code Changes for microsoft-365defender-json-alert-trigger-success-publish (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_id', 'alert_name', 'alert_severity', 'alert_source', 'alert_subject', 'alert_type', 'app', 'categories', 'dest_email_address', 'dest_email_domain', 'dest_ip', 'dest_port', 'domain', 'email_address', 'email_domain', 'email_subject', 'entity_type', 'file_hash', 'file_name', 'file_path', 'hash_sha256', 'host', 'malware_url', 'process_command_line', 'result', 'service_name', 'src_host', 'src_ip', 'src_port', 'tenant_id', 'time', 'user', 'user_sid'] |
| removed_regex_field | account |  | [] |
| added_regex_field | categories |  | ['"Categories":"\[({categories}[^\]]+)"'] |
| added_regex_field | domain |  | ['"AccountDomain":"({domain}[^"]+)"'] |
| added_regex_field | service_name |  | ['"ServiceSource":"({service_name}[^"]+)"'] |
| added_regex_field | tenant_id |  | ['"tenantId":"({tenant_id}[^"]+)"'] |
| added_regex_field | user |  | ['"AccountName":"(ALL|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |