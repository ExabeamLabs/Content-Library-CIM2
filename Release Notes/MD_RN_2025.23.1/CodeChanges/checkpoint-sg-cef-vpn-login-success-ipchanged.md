# Code Changes for checkpoint-sg-cef-vpn-login-success-ipchanged (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'host', 'os', 'src_host', 'src_ip', 'src_port', 'src_translated_ipnum', 'time', 'user'] |
| added_regex_field | dest_host |  | ['\sdvc=({dest_host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(\s+[\w\.:]+=|$)', '\sdvchost=({dest_host}.+?)(\s+[\w\.:]+=|$)'] |
| removed_attribute | DupFields |  | N/A |