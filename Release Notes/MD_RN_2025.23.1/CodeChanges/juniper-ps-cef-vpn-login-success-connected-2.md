# Code Changes for juniper-ps-cef-vpn-login-success-connected-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'email_address', 'email_domain', 'host', 'src_ip', 'src_port', 'src_translated_ip', 'time', 'user'] |
| edit_regex_field | domain |  | ['\suser=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\]+)\\+)?({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))(\s+\w+=|\s*$)'] |
| edit_regex_field | email_address |  | ['\suser=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\]+)\\+)?({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))(\s+\w+=|\s*$)'] |
| edit_regex_field | email_domain |  | ['\suser=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\]+)\\+)?({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))(\s+\w+=|\s*$)'] |
| edit_regex_field | user |  | ['\suser=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\]+)\\+)?({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))(\s+\w+=|\s*$)'] |
| added_regex_field | account |  | ['\suser=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\]+)\\+)?({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))(\s+\w+=|\s*$)'] |
| removed_attribute | DupFields |  | N/A |