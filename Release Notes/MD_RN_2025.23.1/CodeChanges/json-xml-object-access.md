# Code Changes for json-xml-object-access (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_domain', 'dest_login_id', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'file_path', 'key_name', 'key_type', 'login_id', 'operation', 'process_dir', 'process_id', 'process_name', 'process_path', 'provider_name', 'return_code', 'run_level', 'src_domain', 'time', 'user_sid'] |
| removed_regex_field | dest_user |  | [] |
| removed_regex_field | dest_user_full_name |  | [] |
| edit_regex_field | domain |  | ['<Data Name[^<>]+?SubjectDomainName[^<>]+?>({src_domain}({domain}[^<>]+?))</Data>'] |
| removed_regex_field | user |  | [] |
| added_regex_field | src_domain |  | ['<Data Name[^<>]+?SubjectDomainName[^<>]+?>({src_domain}({domain}[^<>]+?))</Data>'] |
| removed_attribute | DupFields |  | N/A |