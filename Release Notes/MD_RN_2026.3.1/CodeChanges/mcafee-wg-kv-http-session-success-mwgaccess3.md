# Code Changes for mcafee-wg-kv-http-session-success-mwgaccess3 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_ip |  | ['mwg:\s+\[.+?\]\s+".*?"\s+[^\s]+\s+\d+\s+(".*?"\s+){4}(\d+\s+){2}(".*?"\s+){4}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?'] |
| edit_regex_field | dest_port |  | ['mwg:\s+\[.+?\]\s+".*?"\s+[^\s]+\s+\d+\s+"\w+\s+(\w+:\/+)?[^\/:]*:({dest_port}\d+)', 'mwg:\s+\[.+?\]\s+".*?"\s+[^\s]+\s+\d+\s+(".*?"\s+){4}(\d+\s+){2}(".*?"\s+){4}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?'] |
| edit_regex_field | url |  | ['mwg:\s+\[.+?\]\s+".*?"\s+[^\s]+\s+\d+\s+"\w+\s+({url}(\w+:\/+)?({web_domain}[^\/:]+)[^\s"]+)'] |
| edit_regex_field | web_domain |  | ['mwg:\s+\[.+?\]\s+".*?"\s+[^\s]+\s+\d+\s+"\w+\s+({url}(\w+:\/+)?({web_domain}[^\/:]+)[^\s"]+)'] |