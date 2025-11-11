# Code Changes for cisco-duo-json-endpoint-authentication-result-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_attribute | Product |  | Duo Access |
| edit_regex_field | src_ip |  | ['"ip":"+(0.0.0.0|null|({src_ip}[a-fA-F:\.\d]+))"', 'exa_json_path=$.auth_device.ip,exa_regex=(0.0.0.0|null|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))(:({src_port}\d+))?'] |
| edit_regex_field | src_port |  | ['exa_json_path=$.auth_device.ip,exa_regex=(0.0.0.0|null|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))(:({src_port}\d+))?'] |