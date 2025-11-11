# Code Changes for juniper-ps-kv-vpn-login-success-23464 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'additional_info', 'agent', 'arg', 'bytes_in', 'bytes_out', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'email_address', 'email_domain', 'firewall', 'host', 'op', 'protocol', 'realm', 'result', 'role', 'session_duration', 'src_host', 'src_ip', 'src_port', 'src_translated_ip', 'time', 'user', 'vpn_client', 'vpn_client_type'] |
| edit_regex_field | domain |  | ['\suser=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\]+)\\+)?({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))(\s+\w+=|\s*$)'] |
| edit_regex_field | email_address |  | ['\suser=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\]+)\\+)?({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))(\s+\w+=|\s*$)'] |
| edit_regex_field | email_domain |  | ['\suser=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\]+)\\+)?({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))(\s+\w+=|\s*$)'] |
| edit_regex_field | user |  | ['\suser=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\]+)\\+)?({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))(\s+\w+=|\s*$)'] |
| added_regex_field | account |  | ['\suser=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\]+)\\+)?({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))(\s+\w+=|\s*$)'] |
| removed_attribute | DupFields |  | N/A |