# Code Changes for microsoft-evsecurity-xml-endpoint-login-4769 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_domain', 'dest_user', 'domain', 'event_code', 'event_name', 'failure_code', 'host', 'result_code', 'run_level', 'service_name', 'src_host', 'src_ip', 'src_port', 'ticket_encryption_type', 'ticket_options', 'time', 'user'] |
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")TargetDomainName(\'|")>(?=\w)({dest_domain}({domain}[^<]+))</Data>', '<Data Name\\*=(\'|")TargetUserName(\'|")>(([^\/<@]+\/+)({src_host}[^<@]+)(@({dest_domain}({domain}[^<]+)))?|(?=\w)({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@({=dest_domain}({=domain}[^<@\s]+?)))?)<\/Data>'] |
| edit_regex_field | result_code |  | ['<Data Name\\*=(\'|")Status(\'|")>({failure_code}({result_code}[^<]+))</Data>'] |
| edit_regex_field | src_host |  | ['<Data Name\\*=(\'|")ServiceName(\'|")>({src_host}[\w\-.]+\$)</Data>', '<Data Name\\*=(\'|")TargetUserName(\'|")>(([^\/<@]+\/+)({src_host}[^<@]+)(@({dest_domain}({domain}[^<]+)))?|(?=\w)({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@({=dest_domain}({=domain}[^<@\s]+?)))?)<\/Data>'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")TargetUserName(\'|")>(([^\/<@]+\/+)({src_host}[^<@]+)(@({dest_domain}({domain}[^<]+)))?|(?=\w)({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@({=dest_domain}({=domain}[^<@\s]+?)))?)<\/Data>'] |
| added_regex_field | dest_domain |  | ['<Data Name\\*=(\'|")TargetDomainName(\'|")>(?=\w)({dest_domain}({domain}[^<]+))</Data>', '<Data Name\\*=(\'|")TargetUserName(\'|")>(([^\/<@]+\/+)({src_host}[^<@]+)(@({dest_domain}({domain}[^<]+)))?|(?=\w)({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@({=dest_domain}({=domain}[^<@\s]+?)))?)<\/Data>'] |
| added_regex_field | dest_user |  | ['<Data Name\\*=(\'|")TargetUserName(\'|")>(([^\/<@]+\/+)({src_host}[^<@]+)(@({dest_domain}({domain}[^<]+)))?|(?=\w)({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@({=dest_domain}({=domain}[^<@\s]+?)))?)<\/Data>'] |
| added_regex_field | failure_code |  | ['<Data Name\\*=(\'|")Status(\'|")>({failure_code}({result_code}[^<]+))</Data>'] |
| removed_attribute | DupFields |  | N/A |