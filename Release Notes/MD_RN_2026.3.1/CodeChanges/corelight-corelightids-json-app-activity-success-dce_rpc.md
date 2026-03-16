# Code Changes for corelight-corelightids-json-app-activity-success-dce_rpc (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed | Conditions |  | ['"_path":', '"_system_name":', 'ts":"'] |
| changed_parsed_fields | N/A |  | ['connection_id', 'dest_ip', 'dest_port', 'event_subtype', 'host', 'interface_name', 'operation', 'sensor_name', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | dest_ip |  | ['"id\.resp_h":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?', "exa_json_path=$.['id.resp_h'],exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"] |
| edit_regex_field | src_ip |  | ['"id\.orig_h":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?', "exa_json_path=$.['id.orig_h'],exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"] |
| added_regex_field | connection_id |  | ['"uid":"({connection_id}[^"]+)'] |
| added_regex_field | dest_port |  | ['"id\.resp_h":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?', '"id\.resp_p":({dest_port}\d+)'] |
| added_regex_field | event_subtype |  | ['"_path":"({event_subtype}[^"]+)'] |
| added_regex_field | host |  | ['"_system_name":"({host}[\w\.\-]+)'] |
| added_regex_field | interface_name |  | ['"endpoint":"({interface_name}[^"]+)'] |
| added_regex_field | operation |  | ['"operation":"({operation}[^"]+)'] |
| added_regex_field | sensor_name |  | ['"_system_name":"({sensor_name}[\w\.\-]+)'] |
| added_regex_field | src_port |  | ['"id\.orig_h":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?', '"id\.orig_p":({src_port}\d+)'] |
| added_regex_field | time |  | ['"ts":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,6}Z)', '"ts_start":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,6}Z)'] |