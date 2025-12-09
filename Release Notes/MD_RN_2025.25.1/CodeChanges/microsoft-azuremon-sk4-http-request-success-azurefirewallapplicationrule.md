# Code Changes for microsoft-azuremon-sk4-http-request-success-azurefirewallapplicationrule (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'category', 'dest_ip', 'dest_port', 'event_name', 'operation', 'provider_name', 'resource', 'resource_group', 'resource_id', 'src_ip', 'src_port', 'subscription_id', 'time', 'url', 'web_domain'] |
| edit_regex_field | web_domain |  | ['"msg":"HTTPS?\s+request from\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s*to\s*(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({web_domain}[\w\-\.]+))(:({dest_port}\d+))?', '\sUrl:\s*({url}(https?:\/+)?({web_domain}[^"\\\/\s]+)[^"\s]*)\.(\s\w+:|\s*$)'] |
| added_regex_field | url |  | ['\sUrl:\s*({url}(https?:\/+)?({web_domain}[^"\\\/\s]+)[^"\s]*)\.(\s\w+:|\s*$)'] |