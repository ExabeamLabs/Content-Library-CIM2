# Code Changes for juniper-ps-cef-vpn-login-success-passed (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'additional_info', 'agent', 'arg', 'bytes_in', 'bytes_out', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'email_address', 'email_domain', 'firewall', 'host', 'op', 'protocol', 'realm', 'result', 'role', 'session_duration', 'src_ip', 'src_port', 'time', 'user', 'vpn_client', 'vpn_client_type'] |
| edit_regex_field | dest_ip |  | ['\sdstip=({host}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))(:({dest_port}\d+))?'] |
| edit_regex_field | dest_port |  | ['\sdstip=({host}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))(:({dest_port}\d+))?', '\sport=({dest_port}\d+)'] |
| edit_regex_field | domain |  | ['\suser=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\]+)\\+)?({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))(\s+\w+=|\s*$)'] |
| edit_regex_field | email_address |  | ['\suser=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\]+)\\+)?({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))(\s+\w+=|\s*$)'] |
| edit_regex_field | email_domain |  | ['\suser=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\]+)\\+)?({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))(\s+\w+=|\s*$)'] |
| edit_regex_field | host |  | ['({host}[\w.\-]+) PulseSecure:', '\sdstip=({host}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))(:({dest_port}\d+))?'] |
| edit_regex_field | user |  | ['\suser=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\]+)\\+)?({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))(\s+\w+=|\s*$)'] |
| added_regex_field | account |  | ['\suser=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\]+)\\+)?({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))(\s+\w+=|\s*$)'] |
| removed_attribute | DupFields |  | N/A |