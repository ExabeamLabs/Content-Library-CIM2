# Code Changes for microsoft-evadfs-xml-ds-object-delete-success-4929 (Parser)

| Code Change | Field Name | 2025.14.1 | 2025.15.1 |
|-------------|------------|-----------|------------|
| changed_parsed_fields | N/A | ['dest_host', 'domain', 'event_code', 'group_domain', 'group_id', 'group_name', 'host', 'login_id', 'privileges', 'process_id', 'result', 'run_level', 'sub_category', 'time', 'user', 'user_sid'] | ['additional_info', 'dest_host', 'domain', 'event_code', 'group_domain', 'group_id', 'group_name', 'host', 'login_id', 'privileges', 'process_id', 'result', 'result_code', 'run_level', 'sub_category', 'time', 'user', 'user_sid'] |
| added_regex_field | additional_info | [] | ['<Data Name=(\'|")SourceAddr(\'|")>({additional_info}[^<\.]+)'] |
| added_regex_field | result_code | [] | ['<Data Name=(\'|")StatusCode(\'|")>({result_code}[^<]+)'] |