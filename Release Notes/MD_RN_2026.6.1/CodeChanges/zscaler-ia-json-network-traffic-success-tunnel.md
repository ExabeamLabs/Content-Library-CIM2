# Code Changes for zscaler-ia-json-network-traffic-success-tunnel (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed | Conditions |  | ['"sourceip":"', '"tunneltype":"', 'Tunnel', 'location'] |
| edit_regex_field | email_address |  | ['exa_json_path=$..user,exa_regex=((\d{1,3}\.){3}\d{1,3}|NA|(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| edit_regex_field | email_domain |  | ['exa_json_path=$..user,exa_regex=((\d{1,3}\.){3}\d{1,3}|NA|(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| edit_regex_field | user |  | ['exa_json_path=$..user,exa_regex=((\d{1,3}\.){3}\d{1,3}|NA|(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |