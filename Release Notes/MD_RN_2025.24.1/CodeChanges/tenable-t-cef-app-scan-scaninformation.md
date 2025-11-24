# Code Changes for tenable-t-cef-app-scan-scaninformation (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_name', 'alert_severity', 'alert_type', 'os', 'result', 'scan_type', 'src_host', 'src_ip', 'src_port', 'time'] |
| added_regex_field | time |  | ['"startScanDateTime":"({time}[^",]+)"'] |
| removed_attribute | DupFields |  | N/A |