# Code Changes for zscaler-ia-cef-http-session-spriv (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_name', 'bytes_in', 'bytes_out', 'categories', 'category', 'department', 'dest_ip', 'dest_port', 'dlp_dict', 'dlp_engine', 'email_address', 'file_ext', 'file_name', 'file_type', 'host', 'http_response_code', 'location', 'location_area', 'malware_family', 'malware_name', 'method', 'mime', 'network_app', 'owner_id', 'protocol', 'proxy_action', 'referrer', 'risk_level', 'risk_score', 'rule', 'severity', 'src_file_name', 'src_host', 'src_ip', 'src_port', 'time', 'uri_path', 'uri_query', 'url', 'user', 'user_agent', 'web_domain', 'web_log_dict'] |
| edit_regex_field | email_address |  | ['\slogin=({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)\s\w+=', '\ssuser=((noauth-protocol[^=]+)?(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)(?<!local)\s)|((\w+[^=]+\->\w+[^=]+)\s|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| removed_regex_field | email_domain |  | [] |
| edit_regex_field | location |  | ['\sspriv=({location_area}({location}[^=]+?))\s\w+='] |
| edit_regex_field | user |  | ['\ssuser=((noauth-protocol[^=]+)?(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)(?<!local)\s)|((\w+[^=]+\->\w+[^=]+)\s|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))', '\ssuser=(NA|None|\$NULL|(\w+[^=]+\->\w+[^=]+)\s|(?![^\s]+@[^\s]+)({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*(\w+=|$)'] |
| added_regex_field | location_area |  | ['\sspriv=({location_area}({location}[^=]+?))\s\w+='] |
| removed_attribute | DupFields |  | N/A |