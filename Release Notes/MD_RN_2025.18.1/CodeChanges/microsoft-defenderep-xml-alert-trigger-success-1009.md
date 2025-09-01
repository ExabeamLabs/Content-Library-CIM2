# Code Changes for microsoft-defenderep-xml-alert-trigger-success-1009 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | alert_name |  | ['<Data Name\\*=(\'|")Threat Name(\'|")>({alert_name}[^<]+)<\/Data>'] |
| edit_regex_field | alert_severity |  | ['<Data Name\\*=(\'|")Severity ID(\'|")>({alert_severity}\d+)<\/Data>', '<Data Name\\*=(\'|")Severity Name(\'|")>({alert_severity}[^<]+)<\/Data>'] |
| edit_regex_field | alert_type |  | ['<Data Name\\*=(\'|")Type Name(\'|")>({alert_type}[^<]+)<\/Data>'] |
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")Detection User(\'|")>(({domain}[^\<]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)<\/Data>', '<Data Name\\*=(\'|")Domain(\'|")>({domain}[^<]+)<\/Data>'] |
| edit_regex_field | threat_id |  | ['<Data Name\\*=(\'|")Threat ID(\'|")>({threat_id}\d+)<\/Data>'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")Detection User(\'|")>(({domain}[^\<]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)<\/Data>', '<Data Name\\*=(\'|")User(\'|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)<\/Data>'] |
| edit_regex_field | user_sid |  | ['<Security UserID\\*=(\'|")({user_sid}[^\'">]+)(\'|")\/>'] |