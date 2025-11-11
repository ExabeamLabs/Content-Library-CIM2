# Code Changes for sentinelone-singularityp-json-alert-trigger-success-url-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_ip', 'domain', 'malware_url', 'process_dir', 'process_name', 'process_path', 'uri_path', 'uri_query', 'url', 'user', 'web_domain'] |
| edit_regex_field | dest_ip |  | ['exa_json_path=$.[\'url.address\'],exa_regex=({malware_url}({url}(\w+:\/\/)?(({dest_ip}[A-Fa-f.:\d]+)|({web_domain}[^\/]+?))({uri_path}\/[^\?]*?)?({uri_query}\?[^"]+)?))$'] |
| edit_regex_field | uri_path |  | ['exa_json_path=$.[\'url.address\'],exa_regex=({malware_url}({url}(\w+:\/\/)?(({dest_ip}[A-Fa-f.:\d]+)|({web_domain}[^\/]+?))({uri_path}\/[^\?]*?)?({uri_query}\?[^"]+)?))$'] |
| edit_regex_field | uri_query |  | ['exa_json_path=$.[\'url.address\'],exa_regex=({malware_url}({url}(\w+:\/\/)?(({dest_ip}[A-Fa-f.:\d]+)|({web_domain}[^\/]+?))({uri_path}\/[^\?]*?)?({uri_query}\?[^"]+)?))$'] |
| edit_regex_field | url |  | ['exa_json_path=$.[\'url.address\'],exa_regex=({malware_url}({url}(\w+:\/\/)?(({dest_ip}[A-Fa-f.:\d]+)|({web_domain}[^\/]+?))({uri_path}\/[^\?]*?)?({uri_query}\?[^"]+)?))$'] |
| edit_regex_field | web_domain |  | ['exa_json_path=$.[\'url.address\'],exa_regex=({malware_url}({url}(\w+:\/\/)?(({dest_ip}[A-Fa-f.:\d]+)|({web_domain}[^\/]+?))({uri_path}\/[^\?]*?)?({uri_query}\?[^"]+)?))$'] |
| added_regex_field | malware_url |  | ['exa_json_path=$.[\'url.address\'],exa_regex=({malware_url}({url}(\w+:\/\/)?(({dest_ip}[A-Fa-f.:\d]+)|({web_domain}[^\/]+?))({uri_path}\/[^\?]*?)?({uri_query}\?[^"]+)?))$'] |
| removed_attribute | DupFields |  | N/A |