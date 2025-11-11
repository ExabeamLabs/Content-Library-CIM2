# Code Changes for microsoft-evsystem-str-ssl-start-fail-36874 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'event_code', 'event_name', 'host', 'time'] |
| edit_regex_field | host |  | ['\s+({dest_host}({host}[\w.\-]+))\s+EvntSLog'] |
| added_regex_field | dest_host |  | ['\s+({dest_host}({host}[\w.\-]+))\s+EvntSLog'] |
| removed_attribute | DupFields |  | N/A |