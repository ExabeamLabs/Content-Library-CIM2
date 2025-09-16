# Code Changes for cisco-ise-str-app-notification-alarm (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed | Conditions |  | ['CISE_Alarm', 'ise'] |
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'event_category', 'event_name', 'failure_reason', 'src_host', 'src_ip', 'src_port'] |
| edit_regex_field | additional_info |  | ['Details=({additional_info}.+?)(?:;|$)', 'Message=({additional_info}[^"]+)(?:;|$)'] |
| edit_regex_field | failure_reason |  | ['Error Message=({failure_reason}.+?)$', 'Failure Reason=({failure_reason}[^\s]+)\s'] |
| edit_regex_field | src_host |  | ['Server=\s*({src_host}.+?)(?:;|$)'] |
| edit_regex_field | src_ip |  | ['NAD Address=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?(?:;|$)', 'NAS IP Address=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?(?:;|$)'] |
| edit_regex_field | src_port |  | ['NAD Address=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?(?:;|$)', 'NAS IP Address=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?(?:;|$)', 'port\s({src_port}\d+)'] |
| added_regex_field | action |  | ['Action=({action}[^,]+)(?:;|$)'] |