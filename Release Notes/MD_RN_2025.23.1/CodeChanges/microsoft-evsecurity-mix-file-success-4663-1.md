# Code Changes for microsoft-evsecurity-mix-file-success-4663-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'access_mask', 'domain', 'event_code', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'file_type', 'host', 'login_id', 'process_dir', 'process_name', 'process_path', 'registry_key', 'registry_path', 'src_domain', 'src_file_ext', 'src_file_name', 'src_file_path', 'src_host', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['"Account":"(({domain}[^\\\s"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)', '<Data Name=("|\')SubjectDomainName("|\')>(?=\w)({domain}({src_domain}[^<]+))<'] |
| edit_regex_field | host |  | ['"Computer":"({src_host}({host}[\w\-.]+?))"', '<Computer>([^<>]+?[\\\/]+)?({src_host}({host}[\w\-.]+))<', 'Computer=({src_host}({host}[\w\-.]*?))\s*\w+='] |
| edit_regex_field | src_domain |  | ['<Data Name=("|\')SubjectDomainName("|\')>(?=\w)({domain}({src_domain}[^<]+))<'] |
| edit_regex_field | src_user |  | ['<Data Name=("|\')SubjectUserName("|\')>(?=\w)({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))<'] |
| edit_regex_field | user |  | ['"Account":"(({domain}[^\\\s"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)', '<Data Name=("|\')SubjectUserName("|\')>(?=\w)({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))<'] |
| added_regex_field | src_host |  | ['"Computer":"({src_host}({host}[\w\-.]+?))"', '<Computer>([^<>]+?[\\\/]+)?({src_host}({host}[\w\-.]+))<', 'Computer=({src_host}({host}[\w\-.]*?))\s*\w+='] |
| removed_attribute | DupFields |  | N/A |