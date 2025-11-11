# Code Changes for mcafee-epo-xml-alert-trigger-success-1027 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_name', 'alert_severity', 'alert_type', 'domain', 'event_code', 'file_dir', 'file_ext', 'file_name', 'hash_md5', 'host', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | alert_type |  | ['<szVirusType>({alert_name}({alert_type}[^<]+))<\/szVirusType>'] |
| added_regex_field | alert_name |  | ['<szVirusType>({alert_name}({alert_type}[^<]+))<\/szVirusType>'] |
| removed_attribute | DupFields |  | N/A |