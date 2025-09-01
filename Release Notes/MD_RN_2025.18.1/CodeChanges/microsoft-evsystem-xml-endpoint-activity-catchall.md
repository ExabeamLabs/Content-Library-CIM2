# Code Changes for microsoft-evsystem-xml-endpoint-activity-catchall (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'client_name', 'email_address', 'error_code', 'event_code', 'event_id', 'event_name', 'full_name', 'host', 'process_guid', 'process_id', 'provider_name', 'result', 'run_level', 'sub_category', 'time', 'user', 'user_sid'] |
| edit_regex_field | additional_info |  | ['<Data Name=(\'|")Subject(\'|")>({additional_info}[^<]+?)\s*<', '<Data>({additional_info}[^<]+)<'] |
| added_regex_field | email_address |  | ['<Data Name=(\'|")AccountName(\'|")>(({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|<]+\.[^\]\s"\\,\|<]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^<]+))<'] |
| added_regex_field | full_name |  | ['<Data Name=(\'|")AccountName(\'|")>(({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|<]+\.[^\]\s"\\,\|<]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^<]+))<'] |
| added_regex_field | user |  | ['<Data Name=(\'|")AccountName(\'|")>(({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|<]+\.[^\]\s"\\,\|<]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^<]+))<'] |