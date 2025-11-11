# Code Changes for microsoft-evsecurity-json-file-success-accessanobject (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'access_mask', 'dest_host', 'domain', 'event_code', 'event_id', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'file_type', 'host', 'login_id', 'process_dir', 'process_name', 'process_path', 'src_domain', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['"Account\\*":\\*"(({domain}[^\\\s"]+)\\+)?({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))', '"SubjectDomainName"\s*:\s*\"({src_domain}({domain}[^\"]+))'] |
| edit_regex_field | host |  | ['"(?:winlog\.)?computer_name\\*":\\*"({dest_host}({host}[\w\-.]+))'] |
| edit_regex_field | user |  | ['"Account\\*":\\*"(({domain}[^\\\s"]+)\\+)?({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))', '"SubjectUserName"\s*:\s*\"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| added_regex_field | dest_host |  | ['"(?:winlog\.)?computer_name\\*":\\*"({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | src_domain |  | ['"SubjectDomainName"\s*:\s*\"({src_domain}({domain}[^\"]+))'] |
| added_regex_field | src_user |  | ['"Account\\*":\\*"(({domain}[^\\\s"]+)\\+)?({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))', '"SubjectUserName"\s*:\s*\"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| removed_attribute | DupFields |  | N/A |