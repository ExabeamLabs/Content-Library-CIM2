# Code Changes for netskope-sc-cef-http-session-success-cloudapp (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_ip |  | ['"dstip":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"', '"page":\s*"({url}(\w+:\/\/)?(({dest_ip}[A-Fa-f.:\d]+)|({web_domain}[^"\/]+))({uri_path}\/[^"\?]*)?({uri_query}\?[^"]+)?)"'] |
| edit_regex_field | uri_path |  | ['"page":\s*"({url}(\w+:\/\/)?(({dest_ip}[A-Fa-f.:\d]+)|({web_domain}[^"\/]+))({uri_path}\/[^"\?]*)?({uri_query}\?[^"]+)?)"'] |
| edit_regex_field | uri_query |  | ['"page":\s*"({url}(\w+:\/\/)?(({dest_ip}[A-Fa-f.:\d]+)|({web_domain}[^"\/]+))({uri_path}\/[^"\?]*)?({uri_query}\?[^"]+)?)"'] |
| edit_regex_field | url |  | ['"page":\s*"({url}(\w+:\/\/)?(({dest_ip}[A-Fa-f.:\d]+)|({web_domain}[^"\/]+))({uri_path}\/[^"\?]*)?({uri_query}\?[^"]+)?)"', '"url":\s*"({url}[^"]+)"'] |
| edit_regex_field | web_domain |  | ['"domain":\s*"({web_domain}[^"]+)"', '"page":\s*"(\w+:\/\/)?({web_domain}[^\\\/"]+)', '"page":\s*"({url}(\w+:\/\/)?(({dest_ip}[A-Fa-f.:\d]+)|({web_domain}[^"\/]+))({uri_path}\/[^"\?]*)?({uri_query}\?[^"]+)?)"'] |