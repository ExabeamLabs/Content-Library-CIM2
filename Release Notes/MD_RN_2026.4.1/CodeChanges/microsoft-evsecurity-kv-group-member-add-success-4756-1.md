# Code Changes for microsoft-evsecurity-kv-group-member-add-success-4756-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'account_name', 'additional_info', 'channel', 'dest_host', 'dest_ip', 'dest_port', 'dest_user_sid', 'domain', 'event_code', 'group_domain', 'group_id', 'group_name', 'host', 'login_id', 'process_guid', 'process_id', 'provider_name', 'src_domain', 'src_ip', 'src_port', 'src_user', 'time', 'user', 'user_dn', 'user_ou', 'user_sid'] |
| added_regex_field | channel |  | ['Channel"?(:|>)"?({channel}[^<"]+)'] |