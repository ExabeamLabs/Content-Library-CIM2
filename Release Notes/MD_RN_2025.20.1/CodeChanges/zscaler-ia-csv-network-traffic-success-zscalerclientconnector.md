# Code Changes for zscaler-ia-csv-network-traffic-success-zscalerclientconnector (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| COULD_NOT_COMPARE | TimeFormat |  | ['MMM d HH:mm:ss yyyy', 'MMM dd HH:mm:ss yyyy'] |
| changed | Conditions |  | ['"ZscalerClientConnector'] |
| edit_regex_field | bytes_in |  | ['\w{3}\s+\d+\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){26}"({bytes_in}\d+)"'] |
| edit_regex_field | bytes_out |  | ['\w{3}\s+\d+\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){27}"({bytes_out}\d+)"'] |
| edit_regex_field | category |  | ['\w{3}\s+\d+\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){22}"({category}[^"]+)"'] |
| edit_regex_field | department |  | ['\w{3}\s+\d+\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){2}"({department}[^"]+)"'] |
| edit_regex_field | dest_ip |  | ['\w{3}\s+\d+\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){9}"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"'] |
| edit_regex_field | dest_port |  | ['\w{3}\s+\d+\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){4}"({dest_port}\d+)"'] |
| edit_regex_field | duration |  | ['\w{3}\s+\d+\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){28}"({duration}[^"]+)"'] |
| edit_regex_field | email_address |  | ['\w{3}\s+\d+\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){1}"({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"'] |
| edit_regex_field | email_domain |  | ['\w{3}\s+\d+\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){1}"({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"'] |
| edit_regex_field | location |  | ['\w{3}\s+\d+\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){3}"({location}[^"]+)"'] |
| edit_regex_field | network_app |  | ['\w{3}\s+\d+\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){20}"({network_app}[^"]+)"'] |
| edit_regex_field | protocol |  | ['\w{3}\s+\d+\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){21}"({protocol}[^"]+)"'] |
| edit_regex_field | rule |  | ['\w{3}\s+\d+\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){25}"({rule}[^"]+)"'] |
| edit_regex_field | service_name |  | ['\w{3}\s+\d+\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){19}"({service_name}[^"]+)"'] |
| edit_regex_field | session_id |  | ['\w{3}\s+\d+\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){30}"({session_id}[^"]+)"'] |
| edit_regex_field | src_host |  | ['\w{3}\s+\d+\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){35}"(NA|({src_host}[\w\-.]+))'] |
| edit_regex_field | src_ip |  | ['\w{3}\s+\d+\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){8}"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"'] |
| edit_regex_field | src_port |  | ['\w{3}\s+\d+\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){5}"({src_port}\d+)"'] |
| edit_regex_field | threat_category |  | ['\w{3}\s+\d+\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){32}"(None|({threat_category}[^"]+))"'] |
| edit_regex_field | time |  | ['({time}\w{3}\s+\d+\s\d\d:\d\d:\d\d\s\d\d\d\d)"'] |
| edit_regex_field | user |  | ['\w{3}\s+\d+\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){34}"(None|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |