# Code Changes for siteminder-symantecsm-str-app-logout-success-authlogout (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'domain', 'full_name', 'group_name', 'host', 'process_name', 'result', 'src_host', 'src_ip', 'src_port', 'time', 'user', 'user_ou'] |
| edit_regex_field | domain |  | ['\sCN=(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^"\\=]+)),OU=({group_name}[^,]+),DC=({domain}[^,]+),DC=(?:[^,]+),DC=({process_name}[^\"]+)[\"\s]+({src_host}[^\"\s]+)\s+\"'] |
| edit_regex_field | full_name |  | ['\sCN=(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^"\\=]+)),OU=({group_name}[^,]+),DC=({domain}[^,]+),DC=(?:[^,]+),DC=({process_name}[^\"]+)[\"\s]+({src_host}[^\"\s]+)\s+\"'] |
| edit_regex_field | group_name |  | ['\sCN=(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^"\\=]+)),OU=({group_name}[^,]+),DC=({domain}[^,]+),DC=(?:[^,]+),DC=({process_name}[^\"]+)[\"\s]+({src_host}[^\"\s]+)\s+\"'] |
| edit_regex_field | process_name |  | ['\sCN=(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^"\\=]+)),OU=({group_name}[^,]+),DC=({domain}[^,]+),DC=(?:[^,]+),DC=({process_name}[^\"]+)[\"\s]+({src_host}[^\"\s]+)\s+\"'] |
| edit_regex_field | src_host |  | ['\sCN=(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^"\\=]+)),OU=({group_name}[^,]+),DC=({domain}[^,]+),DC=(?:[^,]+),DC=({process_name}[^\"]+)[\"\s]+({src_host}[^\"\s]+)\s+\"'] |
| removed_regex_field | top_domain |  | [] |
| edit_regex_field | user |  | [':\s({result}[^:]+?)\s+({host}\S+)\s+\[({time}\d\d\/\w+\/\d\d\d\d:\d\d:\d\d:\d\d (\+|\-)\d+)\] "\s*({user_ou}cn=({user}[\w\.\-\!\#\^\~]{1,40}\$?)[^"]*)"', '\sCN=(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^"\\=]+)),OU=({group_name}[^,]+),DC=({domain}[^,]+),DC=(?:[^,]+),DC=({process_name}[^\"]+)[\"\s]+({src_host}[^\"\s]+)\s+\"'] |