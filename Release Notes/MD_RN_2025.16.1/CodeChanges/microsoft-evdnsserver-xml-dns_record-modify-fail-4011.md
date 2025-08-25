# Code Changes for microsoft-evdnsserver-xml-dns_record-modify-fail-4011 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_network_zone |  | ['<Data Name=(\'|")param2(\'|")>({dest_network_zone}[^<]+)'] |
| edit_regex_field | domain |  | ['<Data Name=(\'|")User(Context|Name)(\'|")>(({domain}[^\\\/<]+?)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)<', '<Data Name=(\'|")param1(\'|")>({domain}[^\s<]+)'] |
| edit_regex_field | failure_reason |  | ['<Data Name=(\'|")param3(\'|")>({failure_reason}[^<]+?)\s*<'] |