# Code Changes for observeit-o-cef-alert-trigger-success-high (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'app', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'host', 'malware_url', 'object', 'operation', 'os', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | alert_name |  | ['CEF:([^\|]*\|){5}({alert_type}({alert_name}[^\|]+))\|({alert_severity}[^\|]+)'] |
| edit_regex_field | alert_severity |  | ['CEF:([^\|]*\|){5}({alert_type}({alert_name}[^\|]+))\|({alert_severity}[^\|]+)', '\WdeviceSeverity=(|({alert_severity}.+?))(\s+\w+=|\s*$)'] |
| added_regex_field | alert_type |  | ['CEF:([^\|]*\|){5}({alert_type}({alert_name}[^\|]+))\|({alert_severity}[^\|]+)'] |
| removed_attribute | DupFields |  | N/A |