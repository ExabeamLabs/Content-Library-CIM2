# Code Changes for microsoft-evsecurity-xml-audit-policy-modify-success-4719 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['category_id', 'channel', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'result', 'run_level', 'src_domain', 'src_host', 'src_user', 'sub_category_id', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |