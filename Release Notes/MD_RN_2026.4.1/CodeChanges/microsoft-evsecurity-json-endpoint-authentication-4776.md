# Code Changes for microsoft-evsecurity-json-endpoint-authentication-4776 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'channel', 'domain', 'email_address', 'email_domain', 'event_code', 'event_id', 'event_name', 'host', 'provider_name', 'result_code', 'severity', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)"'] |