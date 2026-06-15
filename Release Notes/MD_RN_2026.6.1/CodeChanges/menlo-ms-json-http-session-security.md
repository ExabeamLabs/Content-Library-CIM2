# Code Changes for menlo-ms-json-http-session-security (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed | Conditions |  | ['"MSIP"', '"Menlo Security"', '"product":', '"severity":', '"vendor":', '"x-client-ip":'] |
| changed_parsed_fields | N/A |  | ['browser', 'dest_ip', 'dest_port', 'email_address', 'email_domain', 'src_ip', 'src_port', 'user'] |
| edit_regex_field | email_address |  | ['exa_json_path=$.userid,exa_regex=(Unknown|(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| edit_regex_field | email_domain |  | ['exa_json_path=$.userid,exa_regex=(Unknown|(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| edit_regex_field | user |  | ['exa_json_path=$.userid,exa_regex=(Unknown|(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))', 'exa_regex=username="*({user}[\w\.\-\!\#\^\~]{1,40}\$?)"'] |
| added_regex_field | browser |  | ['exa_json_path=$.browser_and_version,exa_regex=(NA|({browser}[^"]+))'] |