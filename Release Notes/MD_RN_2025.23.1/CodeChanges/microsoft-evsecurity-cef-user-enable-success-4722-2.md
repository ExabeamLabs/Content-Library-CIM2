# Code Changes for microsoft-evsecurity-cef-user-enable-success-4722-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_domain', 'dest_host', 'dest_ip', 'dest_port', 'dest_user', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'time', 'user'] |
| edit_regex_field | dest_host |  | ['\sshost=({host}({dest_host}[\w\-.]+?))(\s|0\||$)'] |
| edit_regex_field | dest_ip |  | ['\ssrc=({host}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?))(:({dest_port}\d+))?(\s|0\||$)'] |
| edit_regex_field | dest_port |  | ['\ssrc=({host}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?))(:({dest_port}\d+))?(\s|0\||$)'] |
| added_regex_field | host |  | ['\sshost=({host}({dest_host}[\w\-.]+?))(\s|0\||$)', '\ssrc=({host}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?))(:({dest_port}\d+))?(\s|0\||$)'] |
| removed_attribute | DupFields |  | N/A |