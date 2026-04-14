# Code Changes for microsoft-evsecurity-json-policy-modify-4948 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'domain', 'event_code', 'event_name', 'host', 'log_source', 'login_id', 'rule', 'rule_id', 'src_domain', 'src_ip', 'src_port', 'src_user', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)', 'Channel"?(:|=)"?({channel}[^"<]+)'] |