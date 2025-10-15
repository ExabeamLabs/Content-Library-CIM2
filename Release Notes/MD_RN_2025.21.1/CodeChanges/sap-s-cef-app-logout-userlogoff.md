# Code Changes for sap-s-cef-app-logout-userlogoff (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['activity_id', 'additional_info', 'app', 'category', 'event_code', 'event_name', 'host', 'host_ip', 'src_host', 'src_ip', 'time', 'user'] |
| edit_regex_field | activity_id |  | ['SECUDE\|C-Bus\|[^\|]+\|({event_code}({activity_id}[^\|]+))\|(|({event_name}[^\|]+))\|'] |
| edit_regex_field | event_name |  | ['SECUDE\|C-Bus\|[^\|]+\|({event_code}({activity_id}[^\|]+))\|(|({event_name}[^\|]+))\|'] |
| added_regex_field | event_code |  | ['SECUDE\|C-Bus\|[^\|]+\|({event_code}({activity_id}[^\|]+))\|(|({event_name}[^\|]+))\|'] |
| removed_attribute | DupFields |  | N/A |