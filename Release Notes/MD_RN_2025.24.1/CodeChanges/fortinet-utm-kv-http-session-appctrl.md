# Code Changes for fortinet-utm-kv-http-session-appctrl (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'app', 'auth_server', 'category', 'dest_interface', 'dest_ip', 'dest_port', 'dest_role', 'direction', 'event_name', 'event_subtype', 'host', 'policy_id', 'protocol', 'severity', 'src_interface', 'src_ip', 'src_port', 'src_role', 'time', 'tz', 'uri_path', 'user', 'web_domain'] |
| added_regex_field | dest_interface |  | ['\sdstintf=\\?"?({dest_interface}[^=]+?)\\?"?\s*(\w+=|$)'] |
| added_regex_field | dest_role |  | ['\Wdstintfrole=\"+(undefined|({dest_role}[^\"]+))\"+'] |
| added_regex_field | direction |  | ['\Wdirection=\\?"?(((?i)unknown)|({direction}[^=]+?))\\?"?\s*(\w+=|$)'] |
| added_regex_field | policy_id |  | ['\spolicyid=({policy_id}\d+)'] |
| added_regex_field | severity |  | ['\sapprisk=\\?"?({severity}[^=]+?)\\?"?\s*(\w+=|$)'] |
| added_regex_field | src_interface |  | ['\ssrcintf=\\?"?({src_interface}[^=]+?)\\?"?\s*(\w+=|$)'] |
| added_regex_field | src_role |  | ['\Wsrcintfrole=\"+(undefined|({src_role}[^\"]+))\"+'] |