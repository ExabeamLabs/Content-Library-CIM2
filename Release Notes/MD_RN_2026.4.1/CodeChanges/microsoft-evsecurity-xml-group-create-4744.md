# Code Changes for microsoft-evsecurity-xml-group-create-4744 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_host', 'domain', 'group_domain', 'group_id', 'group_name', 'host', 'login_id', 'process_id', 'result_code', 'run_level', 'src_domain', 'src_user', 'sub_category', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |