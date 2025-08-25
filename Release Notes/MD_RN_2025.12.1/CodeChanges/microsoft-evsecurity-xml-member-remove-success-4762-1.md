# Code Changes for microsoft-evsecurity-xml-member-remove-success-4762-1 (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| changed_parsed_fields | N/A | ['account_id', 'dest_user_sid', 'domain', 'event_code', 'group_domain', 'group_name', 'host', 'login_id', 'process_guid', 'process_id', 'provider_name', 'result', 'run_level', 'sub_category', 'time', 'user', 'user_sid'] | ['account_id', 'dest_user_sid', 'domain', 'event_code', 'group_domain', 'group_name', 'host', 'login_id', 'member', 'process_guid', 'process_id', 'provider_name', 'result', 'run_level', 'sub_category', 'time', 'user', 'user_sid'] |
| added_regex_field | member | [] | ["<Data Name='MemberName'>CN=({member}[^=]+?),CN=Users,"] |