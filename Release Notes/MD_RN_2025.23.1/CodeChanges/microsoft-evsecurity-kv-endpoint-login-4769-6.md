# Code Changes for microsoft-evsecurity-kv-endpoint-login-4769-6 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'dest_host', 'domain', 'event_code', 'event_name', 'failure_code', 'host', 'result_code', 'service_name', 'src_host', 'src_ip', 'src_port', 'ticket_encryption_type', 'ticket_options', 'time', 'user'] |
| edit_regex_field | domain |  | ['Account Name(:|=)\s*(\\r|\\n|\\t)*({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@({domain}[\w._\-]+))?[\s;]*(\\r|\\n|\\t)*Account Domain(:|=)'] |
| edit_regex_field | result_code |  | ['Failure Code(:|=)\s*(\\r|\\n|\\t)*({failure_code}({result_code}.+?))[\s;]*(\\r|\\n|\\t)*Transited Services(:|=)'] |
| edit_regex_field | user |  | ['Account Name(:|=)\s*(\\r|\\n|\\t)*({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@({domain}[\w._\-]+))?[\s;]*(\\r|\\n|\\t)*Account Domain(:|=)'] |
| added_regex_field | account |  | ['Account Name(:|=)\s*(\\r|\\n|\\t)*({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@({domain}[\w._\-]+))?[\s;]*(\\r|\\n|\\t)*Account Domain(:|=)'] |
| added_regex_field | failure_code |  | ['Failure Code(:|=)\s*(\\r|\\n|\\t)*({failure_code}({result_code}.+?))[\s;]*(\\r|\\n|\\t)*Transited Services(:|=)'] |
| removed_attribute | DupFields |  | N/A |