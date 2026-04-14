# Code Changes for microsoft-evsecurity-xml-app-authentication-success-1202 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app_protocol', 'audit_subcategory', 'channel', 'domain', 'email_address', 'endpoint', 'error_code', 'event_code', 'failure_reason', 'host', 'location_information', 'proxy_server', 'relying_party', 'result', 'run_level', 'server', 'src_ip', 'src_port', 'time', 'user', 'user_agent'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |