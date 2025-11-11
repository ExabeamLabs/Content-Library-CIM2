# Code Changes for zeronetworks-zeronetworks-json-app-activity-success-auditlogevent (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['description', 'dest_host', 'domain', 'object_id', 'src_host', 'src_ip', 'src_port', 'user'] |
| removed_regex_field | dest_device_entity_id |  | [] |
| removed_regex_field | source_device_entity_id |  | [] |
| added_regex_field | dest_host |  | ['exa_json_path=$.details,exa_regex=localEntityNames\\":[^\}]+"name\\":\\"({dest_host}[^"\\]+)\\?"'] |
| added_regex_field | domain |  | ['exa_json_path=$.performedBy,exa_regex="name":"(((?i)NT AUTHORITY|NT SERVICE|({domain}[^\\]+))[\\]+)?(local service|(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({user}[\w\.\-]{1,40}\$?))"'] |
| added_regex_field | object_id |  | ['exa_json_path=$.destinationEntitiesList,exa_regex="id":"({object_id}[^"]+)'] |
| added_regex_field | src_host |  | ['exa_json_path=$.details,exa_regex=remoteEntityNames\\":[^\}]+"name\\":\\"({src_host}[^"\\]+)\\?"'] |
| added_regex_field | src_ip |  | ['exa_json_path=$.performedBy,exa_regex="name":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| added_regex_field | src_port |  | ['exa_json_path=$.performedBy,exa_regex="name":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| added_regex_field | user |  | ['exa_json_path=$.performedBy,exa_regex="name":"(((?i)NT AUTHORITY|NT SERVICE|({domain}[^\\]+))[\\]+)?(local service|(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({user}[\w\.\-]{1,40}\$?))"'] |