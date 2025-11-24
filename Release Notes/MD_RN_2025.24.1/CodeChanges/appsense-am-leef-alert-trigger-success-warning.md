# Code Changes for appsense-am-leef-alert-trigger-success-warning (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_name', 'alert_severity', 'alert_type', 'dest_host', 'dest_user_sid', 'domain', 'hash_md5', 'hash_sha1', 'hash_sha256', 'host', 'path', 'process_dir', 'process_name', 'process_path', 'process_vendor', 'time', 'user'] |
| edit_regex_field | alert_name |  | ["Message=(The file )?\'.+?\'( has had)?\s+({alert_type}({alert_name}.+?))\s*(\.|of|for)", "Message=AppSense Application Manager ({alert_type}({alert_name}.+?))\s+(of [^\w]|\'|for)"] |
| edit_regex_field | dest_host |  | ['ComputerName=({host}({dest_host}[^\s]+))'] |
| edit_regex_field | process_dir |  | ['\\'({path}({process_path}({process_dir}(?:(\w+:)*([\\\/]+[^\\\/\'\]\"]+)+)?[\\\/]+)({process_name}[^\\\/\"\]]*?)))(\s+\[\w+:|\')'] |
| edit_regex_field | process_name |  | ['\\'({path}({process_path}({process_dir}(?:(\w+:)*([\\\/]+[^\\\/\'\]\"]+)+)?[\\\/]+)({process_name}[^\\\/\"\]]*?)))(\s+\[\w+:|\')'] |
| edit_regex_field | process_path |  | ['\\'({path}({process_path}({process_dir}(?:(\w+:)*([\\\/]+[^\\\/\'\]\"]+)+)?[\\\/]+)({process_name}[^\\\/\"\]]*?)))(\s+\[\w+:|\')'] |
| added_regex_field | alert_type |  | ["Message=(The file )?\'.+?\'( has had)?\s+({alert_type}({alert_name}.+?))\s*(\.|of|for)", "Message=AppSense Application Manager ({alert_type}({alert_name}.+?))\s+(of [^\w]|\'|for)"] |
| added_regex_field | host |  | ['ComputerName=({host}({dest_host}[^\s]+))'] |
| added_regex_field | path |  | ['\\'({path}({process_path}({process_dir}(?:(\w+:)*([\\\/]+[^\\\/\'\]\"]+)+)?[\\\/]+)({process_name}[^\\\/\"\]]*?)))(\s+\[\w+:|\')'] |
| removed_attribute | DupFields |  | N/A |