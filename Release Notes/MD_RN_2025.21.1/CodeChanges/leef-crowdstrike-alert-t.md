# Code Changes for leef-crowdstrike-alert-t (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_name', 'alert_severity', 'alert_type', 'app', 'category', 'dest_ip', 'dest_port', 'domain', 'hash_md5', 'protocol', 'src_file_name', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | category |  | ['\Wcat=({alert_type}({category}[^\|]+?))\s*(\||\w+=|$|"+\s*$)'] |
| added_regex_field | alert_type |  | ['\Wcat=({alert_type}({category}[^\|]+?))\s*(\||\w+=|$|"+\s*$)'] |
| removed_attribute | DupFields |  | N/A |