# Code Changes for fortinet-fortigate-kv-network-traffic-logid (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed | Conditions |  | [' devid=', ' devname=', ' level=', ' logid='] |
| edit_regex_field | domain |  | ['\suser=\\?"?\s*(N\/A|(?:host\/({src_host}[^"\\]+))|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^="]+))?)\s*\\?"?\s+(\w+=|$)'] |
| edit_regex_field | email_address |  | ['\suser=\\?"?\s*(N\/A|(?:host\/({src_host}[^"\\]+))|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^="]+))?)\s*\\?"?\s+(\w+=|$)'] |
| edit_regex_field | src_host |  | ['\ssrcname=\\?"?(::ffff:)?({src_host}[\w\-.]+?)\\?"?\s+\w+=', '\suser=\\?"?\s*(N\/A|(?:host\/({src_host}[^"\\]+))|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^="]+))?)\s*\\?"?\s+(\w+=|$)'] |
| edit_regex_field | user |  | ['\suser=\\?"?\s*(N\/A|(?:host\/({src_host}[^"\\]+))|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^="]+))?)\s*\\?"?\s+(\w+=|$)'] |