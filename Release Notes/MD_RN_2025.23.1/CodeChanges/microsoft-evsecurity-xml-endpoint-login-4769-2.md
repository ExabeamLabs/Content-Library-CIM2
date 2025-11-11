# Code Changes for microsoft-evsecurity-xml-endpoint-login-4769-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'event_name', 'failure_code', 'host', 'result_code', 'run_level', 'service_name', 'src_ip', 'src_port', 'ticket_encryption_type', 'ticket_options', 'time', 'user'] |
| edit_regex_field | result_code |  | ['Failure Code(:|=)((?-i)\\+[rnt])*\s*({failure_code}({result_code}[^\s:;\\]+))((?-i)\\+[rnt])*\s*[\s;]*[\w\s]+(:|=)'] |
| added_regex_field | failure_code |  | ['Failure Code(:|=)((?-i)\\+[rnt])*\s*({failure_code}({result_code}[^\s:;\\]+))((?-i)\\+[rnt])*\s*[\s;]*[\w\s]+(:|=)'] |
| removed_attribute | DupFields |  | N/A |