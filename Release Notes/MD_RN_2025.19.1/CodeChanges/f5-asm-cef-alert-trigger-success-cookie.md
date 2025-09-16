# Code Changes for f5-asm-cef-alert-trigger-success-cookie (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_name', 'dest_ip', 'dest_port', 'host', 'malware_url', 'method', 'protocol', 'referrer', 'result_reason', 'severity', 'src_ip', 'src_port', 'time', 'user', 'user_agent', 'web_domain'] |
| edit_regex_field | additional_info |  | ['\sASM:(\"[^\"]*\",){17}\"({additional_info}[\S\s]+(?:\\r\\n\\r\\n))\",\"\w+'] |
| edit_regex_field | alert_name |  | ['<viol_name>({alert_name}[^<]+)<\/viol_name>', '\sASM:(\"[^\"]*\",){8}\"({alert_name}(?!\d+(?:\.\d+){3})[^"]+)'] |
| removed_regex_field | dest_host |  | [] |
| edit_regex_field | dest_port |  | ['\sASM:(\"[^\"]*\",){2}\"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?', '\sASM:(\"[^\"]*\",){3}\"({dest_port}\d+)'] |
| removed_regex_field | domain |  | [] |
| edit_regex_field | host |  | ['\w+\s\d+\s\d+:\d+:\d+\s({host}[\w\.]+)\sASM:'] |
| edit_regex_field | protocol |  | ['\sASM:(\"[^\"]*\",){15}\"({protocol}[^\"]+)"', '\sASM:(\"[^\"]*\",){5}\"({protocol}[^\"]+)"'] |
| edit_regex_field | src_ip |  | ['(\\r\\n|\s)X-Forwarded-For:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?(\\r\\n\\r\\n|\s+)', '\sASM:(\"[^\"]*\",){3}\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"', '\sASM:(\"[^\"]*\",){8}\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"'] |
| edit_regex_field | src_port |  | ['(\\r\\n|\s)X-Forwarded-For:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?(\\r\\n\\r\\n|\s+)', '\sASM:(\"[^\"]*\",){3}\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"', '\sASM:(\"[^\"]*\",){8}\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"'] |
| edit_regex_field | user |  | ['\sASM:(\"[^\"]*\",){8}"([\w\s\,\/\-]+)","({user}[\w\.\-\!\#\^\~]{1,40}\$?)"'] |
| added_regex_field | action |  | ['(\d+\.){3}\d+\\r\\n\\r\\n\",\"({action}[^"]+)'] |
| added_regex_field | method |  | ['\sASM:(\"[^\"]*\",){12}\"({method}[^"]+)'] |
| added_regex_field | referrer |  | ['(\\r\\n|\s)Referer:\s*({referrer}[^"]+?)((\\r\\n|\s+)[\w\-]+:|\")'] |
| added_regex_field | result_reason |  | ['\sASM:\"({result_reason}[^\"]+)"'] |
| added_regex_field | severity |  | ['(?:\\r\\n|\s)X-Forwarded-For:\s*(?:\d+\.){3}\d+\\r\\n\\r\\n\",(?:"[^"]+",){5}\"({severity}[^"]+)', '\<\/html\>\\r\\n\",(?:\"[^"]+\",){3}\"({severity}[^"]+)'] |
| added_regex_field | web_domain |  | ['(\\r\\n|\s)Host:\s*({web_domain}[\w\-\.]+?)((\\r\\n|\s+)[\w\-]+:|\")'] |