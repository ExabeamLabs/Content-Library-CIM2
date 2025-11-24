# Code Changes for delinea-secretserver-cef-user-switch-success-checkout (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'account_domain', 'dest_domain', 'dest_email_address', 'dest_host', 'dest_user', 'domain', 'email_address', 'host', 'safe_value', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | dest_domain |  | ['\sfname=((({account_domain}({dest_domain}[^\\=\s]+))(\\)+)?({dest_email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({=account_domain}({=dest_domain}[^=\\]+))(\\+))?({account}({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s+\w+='] |
| edit_regex_field | dest_email_address |  | ['\sfname=((({account_domain}({dest_domain}[^\\=\s]+))(\\)+)?({dest_email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({=account_domain}({=dest_domain}[^=\\]+))(\\+))?({account}({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s+\w+='] |
| edit_regex_field | dest_user |  | ['\sfname=((({account_domain}({dest_domain}[^\\=\s]+))(\\)+)?({dest_email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({=account_domain}({=dest_domain}[^=\\]+))(\\+))?({account}({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s+\w+='] |
| edit_regex_field | host |  | ['\d{2}:\d{2}:\d{2} ({dest_host}({host}[\w\-.]+)) CEF:', '\sdvc=({dest_host}({host}[^\s]+))', '\sdvchost=({dest_host}({host}[^\s]+))'] |
| added_regex_field | account |  | ['\sfname=((({account_domain}({dest_domain}[^\\=\s]+))(\\)+)?({dest_email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({=account_domain}({=dest_domain}[^=\\]+))(\\+))?({account}({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s+\w+='] |
| added_regex_field | account_domain |  | ['\sfname=((({account_domain}({dest_domain}[^\\=\s]+))(\\)+)?({dest_email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({=account_domain}({=dest_domain}[^=\\]+))(\\+))?({account}({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s+\w+='] |
| added_regex_field | dest_host |  | ['\d{2}:\d{2}:\d{2} ({dest_host}({host}[\w\-.]+)) CEF:', '\sdvc=({dest_host}({host}[^\s]+))', '\sdvchost=({dest_host}({host}[^\s]+))'] |
| removed_attribute | DupFields |  | N/A |