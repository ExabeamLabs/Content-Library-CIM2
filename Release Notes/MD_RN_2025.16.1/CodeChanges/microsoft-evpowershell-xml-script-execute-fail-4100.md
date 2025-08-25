# Code Changes for microsoft-evpowershell-xml-script-execute-fail-4100 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | alert_severity |  | ['<Data Name=(\'|")ContextInfo(\'|")>\s*Severity = ({alert_severity}[^\s]+)'] |
| edit_regex_field | command |  | ['<Data Name=(\'|")ContextInfo(\'|")>[^@]+?Command Name\s*=\s*(|({command}[^=]+?))\s*Command Type ='] |
| edit_regex_field | command_type |  | ['<Data Name=(\'|")ContextInfo(\'|")>[^@]+?Command Type\s*=\s*(|({command_type}[^=]+?))\s*Script Name'] |
| edit_regex_field | domain |  | ['<Data Name=(\'|")ContextInfo(\'|")>[^@]+?User\s*=\s*(({domain}[^=]+?)[\\\/]+)?(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\\r|\\n|\\t)*\s*(Connected User|Shell ID) ='] |
| edit_regex_field | process_dir |  | ['<Data Name=(\'|")ContextInfo(\'|")>[^@]+?Host Application\s*=\s*({process_path}(({process_dir}[^\;=\s]+)[\\\/]+)?({process_name}[^\s]+))[^\n]+?\s+Engine Version ='] |
| edit_regex_field | process_name |  | ['<Data Name=(\'|")ContextInfo(\'|")>[^@]+?Host Application\s*=\s*({process_path}(({process_dir}[^\;=\s]+)[\\\/]+)?({process_name}[^\s]+))[^\n]+?\s+Engine Version ='] |
| edit_regex_field | process_path |  | ['<Data Name=(\'|")ContextInfo(\'|")>[^@]+?Host Application\s*=\s*({process_path}(({process_dir}[^\;=\s]+)[\\\/]+)?({process_name}[^\s]+))[^\n]+?\s+Engine Version ='] |
| edit_regex_field | script_name |  | ['<Data Name=(\'|")ContextInfo(\'|")>[^@]+?Script Name\s*=\s+({script_name}\S[^=]+?)\s+Command Path ='] |
| edit_regex_field | user |  | ['<Data Name=(\'|")ContextInfo(\'|")>[^@]+?User\s*=\s*(({domain}[^=]+?)[\\\/]+)?(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\\r|\\n|\\t)*\s*(Connected User|Shell ID) ='] |