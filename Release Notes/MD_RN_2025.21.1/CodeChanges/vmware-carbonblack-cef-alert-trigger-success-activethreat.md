# Code Changes for vmware-carbonblack-cef-alert-trigger-success-activethreat (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_id', 'alert_name', 'alert_severity', 'alert_type', 'dest_host', 'host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | host |  | ['(\s|\|)dvchost=({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | dest_host |  | ['(\s|\|)dvchost=({dest_host}({host}[\w\-.]+))'] |
| removed_attribute | DupFields |  | N/A |