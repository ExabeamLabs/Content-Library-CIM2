# Code Changes for microsoft-evsecurity-xml-endpoint-login-4768 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_type', 'channel', 'dest_domain', 'dest_email_address', 'dest_user', 'domain', 'email_address', 'event_code', 'event_name', 'host', 'opcode', 'result_code', 'run_level', 'service_name', 'src_ip', 'src_port', 'ticket_encryption_type', 'ticket_options', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |