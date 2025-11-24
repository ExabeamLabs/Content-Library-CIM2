# Code Changes for rubrik-cdm-json-app-success-cloudsummary (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'dest_ip', 'failure_reason', 'host', 'result'] |
| edit_regex_field | dest_ip |  | ['exa_regex="summary":".*?Host\s*\'(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}({host}[\w\-\.]+)))\''] |
| edit_regex_field | host |  | ['exa_regex="location":"({dest_host}({host}[\w\-\.]+))', 'exa_regex="summary":".*?Host\s*\'(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}({host}[\w\-\.]+)))\''] |
| added_regex_field | dest_host |  | ['exa_regex="location":"({dest_host}({host}[\w\-\.]+))', 'exa_regex="summary":".*?Host\s*\'(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}({host}[\w\-\.]+)))\''] |
| removed_attribute | DupFields |  | N/A |