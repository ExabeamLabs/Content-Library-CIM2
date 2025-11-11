# Code Changes for cisco-ac-xml-vpn-login-success-2039 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'event_code', 'event_id', 'event_name', 'file_dir', 'file_ext', 'file_hash', 'file_name', 'file_path', 'host', 'process_id', 'provider_name', 'result', 'thread_id', 'time', 'user', 'user_sid'] |
| added_regex_field | dest_host |  | ['<Computer>({dest_host}[^<>]+?)<\/Computer>'] |
| removed_attribute | DupFields |  | N/A |