# Code Changes for microsoft-evsecurity-xml-radius-traffic-627 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_ip', 'dest_port', 'domain', 'event_code', 'event_name', 'failure_reason', 'host', 'location', 'policy_name', 'result', 'run_level', 'time', 'user', 'user_sid', 'user_type', 'user_upn'] |
| edit_regex_field | user |  | ['Account Name:\s*(({user_upn}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+(\.[^\]\s"\\,\|]+)?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*Account Domain', 'Account Name:\s*({user_type}[^\s:]+?)\/({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\.[^:\.\s]+?)*\s*Account Domain'] |
| edit_regex_field | user_upn |  | ['Account Name:\s*(({user_upn}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+(\.[^\]\s"\\,\|]+)?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*Account Domain'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |