# Code Changes for microsoft-evsecurity-kv-user-switch-success-4648-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_domain', 'dest_host', 'dest_service_name', 'dest_user', 'domain', 'event_code', 'host', 'login_id', 'process_dir', 'process_id', 'process_name', 'process_path', 'result', 'src_domain', 'src_ip', 'src_port', 'src_user', 'time', 'user'] |
| edit_regex_field | domain |  | ['Message=.+?\s({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s({domain}[^\s]+)\s({login_id}[^\s]+)\s\{([^\}]+)\}\s({dest_user}[^\s]+)\s({dest_domain}[^\s]+)\s\{.*?\}\s({dest_service_name}[^\s]+)\w.*?\s.*?\s({process_path}({process_dir}[^\s]+[\\\/]+)({process_name}[^\s\\\/]+))', '\sSubjectDomainName=({domain}({src_domain}[^=]+?))\s\w+='] |
| edit_regex_field | host |  | ['\s+Computer=({dest_host}({host}[\w.\-]+))'] |
| edit_regex_field | src_domain |  | ['\sSubjectDomainName=({domain}({src_domain}[^=]+?))\s\w+='] |
| edit_regex_field | src_user |  | ['\sSubjectUserName=({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | user |  | ['Message=.+?\s({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s({domain}[^\s]+)\s({login_id}[^\s]+)\s\{([^\}]+)\}\s({dest_user}[^\s]+)\s({dest_domain}[^\s]+)\s\{.*?\}\s({dest_service_name}[^\s]+)\w.*?\s.*?\s({process_path}({process_dir}[^\s]+[\\\/]+)({process_name}[^\s\\\/]+))', '\sSubjectUserName=({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| added_regex_field | dest_host |  | ['\s+Computer=({dest_host}({host}[\w.\-]+))'] |
| removed_attribute | DupFields |  | N/A |