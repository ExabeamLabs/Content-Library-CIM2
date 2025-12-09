# Code Changes for cisco-duo-json-endpoint-authentication-result-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'browser', 'browser_version', 'domain', 'email_address', 'email_domain', 'factor', 'failure_reason', 'host', 'mfa_country', 'mfa_device', 'os', 'os_version', 'result_reason', 'service_name', 'src_country', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | src_ip |  | ['"ip":"+(0.0.0.0|null|({src_ip}[a-fA-F:\.\d]+))"', 'exa_json_path=$.access_device.ip,exa_regex=(0.0.0.0|null|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))(:({src_port}\d+))?'] |
| added_regex_field | src_port |  | ['exa_json_path=$.access_device.ip,exa_regex=(0.0.0.0|null|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))(:({src_port}\d+))?'] |