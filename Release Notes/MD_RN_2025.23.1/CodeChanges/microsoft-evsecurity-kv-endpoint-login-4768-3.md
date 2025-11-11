# Code Changes for microsoft-evsecurity-kv-endpoint-login-4768-3 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'auth_type', 'domain', 'event_code', 'event_name', 'host', 'result_code', 'service_name', 'src_ip', 'src_port', 'ticket_encryption_type', 'ticket_options', 'time', 'user', 'user_sid'] |
| edit_regex_field | user |  | ['Account Name(:|=)\s*(\\t|\\r|\\n)*({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(?:@.+?)?[\s;]*(\\t|\\r|\\n)*"?\s*Supplied Realm Name', 'exa_json_path=$.Message,exa_regex=Account Name(:|=)\s*(\\t|\\r|\\n)*({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(?:@.+?)?[\s;]*(\\t|\\r|\\n)*"?\s*Supplied Realm Name'] |
| added_regex_field | account |  | ['Account Name(:|=)\s*(\\t|\\r|\\n)*({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(?:@.+?)?[\s;]*(\\t|\\r|\\n)*"?\s*Supplied Realm Name', 'exa_json_path=$.Message,exa_regex=Account Name(:|=)\s*(\\t|\\r|\\n)*({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(?:@.+?)?[\s;]*(\\t|\\r|\\n)*"?\s*Supplied Realm Name'] |
| removed_attribute | DupFields |  | N/A |