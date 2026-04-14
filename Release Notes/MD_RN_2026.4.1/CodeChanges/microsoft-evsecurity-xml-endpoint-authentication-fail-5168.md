# Code Changes for microsoft-evsecurity-xml-endpoint-authentication-fail-5168 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_host', 'domain', 'host', 'login_id', 'run_level', 'src_domain', 'src_host', 'src_ip', 'src_user', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |