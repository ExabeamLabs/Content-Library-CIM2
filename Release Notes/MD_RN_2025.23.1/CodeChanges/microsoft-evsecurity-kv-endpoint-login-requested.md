# Code Changes for microsoft-evsecurity-kv-endpoint-login-requested (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'auth_type', 'dest_ip', 'dest_port', 'domain', 'event_code', 'event_name', 'failure_code', 'host', 'result_code', 'time', 'user', 'user_sid'] |
| edit_regex_field | result_code |  | ['Result Code(:|=)\s*(\\t)?({failure_code}({result_code}[^\s].+?))[\s;]*?(\\r\s\\t)*?Ticket Encryption Type(:|=)'] |
| edit_regex_field | user |  | ['Account Name(:|=)\s*(\\t)?({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(?:@.+?)?[\s;]*(\\r\s\\t)*?Supplied Realm Name'] |
| added_regex_field | account |  | ['Account Name(:|=)\s*(\\t)?({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(?:@.+?)?[\s;]*(\\r\s\\t)*?Supplied Realm Name'] |
| added_regex_field | failure_code |  | ['Result Code(:|=)\s*(\\t)?({failure_code}({result_code}[^\s].+?))[\s;]*?(\\r\s\\t)*?Ticket Encryption Type(:|=)'] |
| removed_attribute | DupFields |  | N/A |