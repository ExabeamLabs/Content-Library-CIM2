# Code Changes for aws-waf-json-http-session-httprequest (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'action', 'aws_account', 'browser', 'dest_host', 'dest_ip', 'dest_port', 'host', 'method', 'mime', 'os', 'protocol', 'referrer', 'rule', 'rule_id', 'src_ip', 'src_port', 'time', 'uri_path', 'uri_query', 'user', 'user_agent', 'web_domain'] |
| edit_regex_field | dest_host |  | ['"name"+:"+(?i)Host"+,"+value"+:"+(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({web_domain}[^="]+?\.(\d+|([^\/\.\s"]+?)))|({dest_host}[\w\-\.]+))[\\\/\s:"]'] |
| edit_regex_field | dest_ip |  | ['"name"+:"+(?i)Host"+,"+value"+:"+(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({web_domain}[^="]+?\.(\d+|([^\/\.\s"]+?)))|({dest_host}[\w\-\.]+))[\\\/\s:"]'] |
| edit_regex_field | dest_port |  | ['"name"+:"+(?i)Host"+,"+value"+:"+(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({web_domain}[^="]+?\.(\d+|([^\/\.\s"]+?)))|({dest_host}[\w\-\.]+))[\\\/\s:"]'] |
| removed_regex_field | top_domain |  | [] |
| edit_regex_field | web_domain |  | ['"name"+:"+(?i)Host"+,"+value"+:"+(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({web_domain}[^="]+?\.(\d+|([^\/\.\s"]+?)))|({dest_host}[\w\-\.]+))[\\\/\s:"]'] |