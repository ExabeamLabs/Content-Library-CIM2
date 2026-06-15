# Code Changes for juniper-ps-cef-vpn-login-success-passed (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | account |  | ['\suser=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\]+)\\+)?({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))(\s+\w+=|\s*$)'] |
| edit_regex_field | domain |  | ['\suser=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\]+)\\+)?({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))(\s+\w+=|\s*$)'] |
| edit_regex_field | email_address |  | ['\suser=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\]+)\\+)?({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))(\s+\w+=|\s*$)'] |
| edit_regex_field | email_domain |  | ['\suser=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\]+)\\+)?({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))(\s+\w+=|\s*$)'] |
| edit_regex_field | user |  | ['\suser=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\]+)\\+)?({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))(\s+\w+=|\s*$)'] |