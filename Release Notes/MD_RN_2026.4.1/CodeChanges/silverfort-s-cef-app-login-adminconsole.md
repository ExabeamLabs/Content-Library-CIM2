# Code Changes for silverfort-s-cef-app-login-adminconsole (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'app', 'dest_host', 'domain', 'email_address', 'host', 'ioc', 'policy_id', 'result', 'severity', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | action |  | ['cs2="?({action}[^"]+)"?\scs3Label'] |
| edit_regex_field | app |  | ['app="?(n\/a|({app}[^"]+))"?\scs1Label'] |
| edit_regex_field | dest_host |  | ['dhost="?(n\/a|({dest_host}[\w\-\.]+))'] |
| edit_regex_field | domain |  | ['sntdom="?({domain}[^"]+)"\sshost', 'sntdom="?({domain}[^"]+)\sshost'] |
| edit_regex_field | email_address |  | ['suser="?(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"?\ssntdom='] |
| removed_regex_field | email_domain |  | [] |
| edit_regex_field | src_host |  | ['shost="?(n\/a|({src_host}[\w\-\.]+))'] |
| edit_regex_field | src_ip |  | ['src="?(n\/a|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)'] |
| edit_regex_field | src_port |  | ['src="?(n\/a|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)'] |
| edit_regex_field | time |  | ['"rt="?({time}\d+)"', 'rt=({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d.\d\d\d)'] |
| edit_regex_field | user |  | ['suser="?(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"?\ssntdom='] |
| added_regex_field | ioc |  | ['cs7="?({ioc}[^"]+)"?\scs8Label'] |
| added_regex_field | policy_id |  | ['cs4="?({policy_id}[^"]+)"?\scs5Label'] |
| added_regex_field | result |  | ['cs5="?(n\/a|({result}[^"]+))"?\scs6Label'] |
| added_regex_field | severity |  | ['cs1="?({severity}[^"]+)"?\scs2Label'] |