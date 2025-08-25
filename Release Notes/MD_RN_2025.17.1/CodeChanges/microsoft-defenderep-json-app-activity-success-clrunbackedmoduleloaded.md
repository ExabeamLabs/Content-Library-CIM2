# Code Changes for microsoft-defenderep-json-app-activity-success-clrunbackedmoduleloaded (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['"InitiatingProcessAccountDomain":\s*"(-|({domain}[^"]+))"', 'exa_json_path=$..InitiatingProcessAccountDomain,exa_regex=(-|({domain}[^$"]+))$'] |
| edit_regex_field | full_name |  | ['InitiatingProcessAccountName":\s*"(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|Système|system|local service|-|({user}[\w\.\-\!\#\^\~]{1,40}\$?)"|({full_name}[^"]+))', 'exa_json_path=$..InitiatingProcessAccountName,exa_regex=(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|Système|system|local service|-|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^",]+))'] |
| edit_regex_field | user |  | ['InitiatingProcessAccountName":\s*"(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|Système|system|local service|-|({user}[\w\.\-\!\#\^\~]{1,40}\$?)"|({full_name}[^"]+))', 'exa_json_path=$..InitiatingProcessAccountName,exa_regex=(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|Système|system|local service|-|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^",]+))'] |