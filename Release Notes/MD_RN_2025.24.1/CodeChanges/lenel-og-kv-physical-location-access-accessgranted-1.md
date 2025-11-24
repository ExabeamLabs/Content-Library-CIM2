# Code Changes for lenel-og-kv-physical-location-access-accessgranted-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| COULD_NOT_COMPARE | TimeFormat |  | ['yyyy-MM-dd HH:mm:ss.S', "yyyy-MM-dd'T'HH:mm:ss.SSSZ"] |
| changed | Conditions |  | ['EVDESCR', 'SSNO'] |
| changed_parsed_fields | N/A |  | ['action', 'badge_id', 'devid', 'first_name', 'last_name', 'location_building', 'location_door', 'seq_num', 'serial_num', 'time', 'user_id'] |
| edit_regex_field | action |  | ['\WEVDESCR(":|=)"({action}[^"]+)'] |
| edit_regex_field | badge_id |  | ['\WCARDNUM(":|=)"({badge_id}[^"]+)'] |
| edit_regex_field | devid |  | ['\WDEVID(":|=)"?({devid}[^",]+)'] |
| removed_regex_field | direction |  | [] |
| edit_regex_field | first_name |  | ['\WFIRSTNAME(":|=)"({first_name}[^"]+?)\s*"'] |
| edit_regex_field | last_name |  | ['\WLASTNAME(":|=)"({last_name}[^"]+?)\s*"'] |
| edit_regex_field | location_building |  | ['\WNAME(":|=)"({location_building}[^"]+)'] |
| edit_regex_field | location_door |  | ['\WREADERDESC(":|=)"({location_door}[^"]+)'] |
| edit_regex_field | seq_num |  | ['\WSEQ(":|=)"({seq_num}\d+)'] |
| edit_regex_field | serial_num |  | ['\WSERIALNUM(":|=)"?({serial_num}[^",]+)'] |
| edit_regex_field | time |  | ['EventDateTime(":|=)"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)', '\WEVENT_LOCAL_TIME(":|=)"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+)'] |
| removed_regex_field | user |  | [] |
| added_regex_field | user_id |  | ['\WSSNO(":|=)"({user_id}[^"]+)'] |