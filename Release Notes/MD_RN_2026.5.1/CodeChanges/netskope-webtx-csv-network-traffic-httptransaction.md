# Code Changes for netskope-webtx-csv-network-traffic-httptransaction (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'browser', 'bytes', 'category', 'connection_type', 'country', 'dest_ip', 'dest_port', 'device_name', 'domain', 'email_address', 'host', 'http_response_code', 'method', 'mime', 'os', 'protocol', 'referrer', 'src_ip', 'src_port', 'time', 'traffic_type', 'uri', 'uri_path', 'url', 'user', 'user_agent', 'web_content_type', 'web_domain'] |
| edit_regex_field | email_address |  | [',(-|(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))),(\d\d\d\d-\d\d-\d\d),(-|({http_response_code}\d+))'] |
| removed_regex_field | email_domain |  | [] |
| edit_regex_field | http_response_code |  | [',(-|(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))),(\d\d\d\d-\d\d-\d\d),(-|({http_response_code}\d+))', ',(\d\d\d\d-\d\d-\d\d),(-|\d+),(-,|"+(.+?)"+,|([^,]*),){3}(-|({http_response_code}\d+))'] |
| edit_regex_field | user |  | [',(-|(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))),(\d\d\d\d-\d\d-\d\d),(-|({http_response_code}\d+))'] |
| added_regex_field | uri_path |  | [',(\d\d\d\d-\d\d-\d\d),(-|\d+),(-,|"+(.+?)"+,|([^,]*),){62}(-|({uri_path}[^\s,]*))'] |
| added_regex_field | url |  | [',(\d\d\d\d-\d\d-\d\d),(-|\d+),(-,|"+(.+?)"+,|([^,]*),){63}(-|"({url}[^"]+)",|({=url}[^,]+),)'] |
| added_regex_field | web_domain |  | [',(\d\d\d\d-\d\d-\d\d),(-|\d+),(-,|"+(.+?)"+,|([^,]*),){63}(-,|[^\/,]+\/+({web_domain}[^\/]+))'] |