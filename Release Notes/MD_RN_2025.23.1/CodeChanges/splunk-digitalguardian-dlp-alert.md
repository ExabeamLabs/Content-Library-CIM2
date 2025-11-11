# Code Changes for splunk-digitalguardian-dlp-alert (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_name', 'alert_severity', 'alert_type', 'bytes', 'dest_ip', 'dest_port', 'device_id', 'domain', 'file_name', 'host', 'os', 'process_name', 'protocol', 'src_host', 'target', 'time', 'user'] |
| edit_regex_field | host |  | ['[^_]Computer_Name="([^\/\\"]+[\/\\]+)?({src_host}({host}[\w\-\.]+))"'] |
| added_regex_field | src_host |  | ['[^_]Computer_Name="([^\/\\"]+[\/\\]+)?({src_host}({host}[\w\-\.]+))"'] |
| removed_attribute | DupFields |  | N/A |