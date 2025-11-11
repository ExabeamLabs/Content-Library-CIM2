# Code Changes for microsoft-evsecurity-kv-file-read-success-4663-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'access_mask', 'domain', 'event_code', 'file_dir', 'file_ext', 'file_name', 'file_path', 'file_type', 'host', 'login_id', 'object_server', 'process_dir', 'process_name', 'process_path', 'registry_key', 'registry_path', 'src_domain', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['SubjectDomainName:({src_domain}({domain}[^:,]+?)),'] |
| edit_regex_field | user |  | ['SubjectUserName:({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)),'] |
| added_regex_field | src_domain |  | ['SubjectDomainName:({src_domain}({domain}[^:,]+?)),'] |
| added_regex_field | src_user |  | ['SubjectUserName:({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)),'] |
| removed_attribute | DupFields |  | N/A |