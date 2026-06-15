# Code Changes for zscaler-ia-kv-network-traffic-success-tunnel (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed | Conditions |  | ['Tunnel', 'location', 'sourceip=', 'tunneltype='] |
| edit_regex_field | email_address |  | ['(vpncredentialname|user)=((\d{1,3}\.){3}\d{1,3}|NA|(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| edit_regex_field | email_domain |  | ['(vpncredentialname|user)=((\d{1,3}\.){3}\d{1,3}|NA|(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| edit_regex_field | src_port |  | ['sourceport=({src_port}\d+)\s+', 'srcport=({src_port}\d+)\s+'] |
| edit_regex_field | time |  | ['({time}\w+\s+\w+\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)', 'datetime=({time}\w+\s+\w+\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)'] |
| edit_regex_field | user |  | ['(vpncredentialname|user)=((\d{1,3}\.){3}\d{1,3}|NA|(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |