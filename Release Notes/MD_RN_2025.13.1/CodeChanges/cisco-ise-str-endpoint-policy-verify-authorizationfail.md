# Code Changes for cisco-ise-str-endpoint-policy-verify-authorizationfail (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed | Conditions |  | ['%SESSION_MGR-5-FAIL:', 'Authorization failed'] |
| changed_parsed_fields | N/A |  | ['event_category', 'event_name', 'failure_reason', 'host_ip', 'interface', 'result', 'session_id', 'src_mac', 'time'] |
| edit_regex_field | event_name |  | ['({event_name}Authorization failed)'] |
| edit_regex_field | src_mac |  | ['for client\s+\(({src_mac}([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})\)'] |
| added_regex_field | host_ip |  | ['host\s*=\s*({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))'] |
| added_regex_field | interface |  | ['Interface\s+({interface}[^\s]+)'] |
| edit_attribute | activity_type |  | ['endpoint-authentication:fail'] |
| edit_attribute | legacy_activity_type |  | ['nac-failed-logon'] |