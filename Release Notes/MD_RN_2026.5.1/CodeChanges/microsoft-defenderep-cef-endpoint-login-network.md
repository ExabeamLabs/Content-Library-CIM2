# Code Changes for microsoft-defenderep-cef-endpoint-login-network (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_ip', 'dest_port', 'device_id', 'domain', 'event_name', 'failure_reason', 'full_name', 'hash_md5', 'host', 'login_id', 'login_type_text', 'process_command_line', 'process_dir', 'process_id', 'process_name', 'process_path', 'protocol', 'result', 'tenant_id', 'time', 'user'] |
| edit_regex_field | user |  | ['"AccountName":"((email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))', '"AccountName":"(-|NA|({full_name}[^"\s]+\s[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"', 'exa_json_path=$..AccountName,exa_regex=(-|NA|({full_name}[^"\s]+\s[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))', 'exa_json_path=$.AccountName,exa_regex=(-|NA|({full_name}[^"\s]+\s[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| added_regex_field | tenant_id |  | ['"tenantId":\s*"({tenant_id}[^"]+)"'] |