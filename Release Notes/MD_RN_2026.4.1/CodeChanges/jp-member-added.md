# Code Changes for jp-member-added (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'group_domain', 'group_id', 'group_name', 'group_type', 'login_id', 'user_dn', 'user_ou'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |