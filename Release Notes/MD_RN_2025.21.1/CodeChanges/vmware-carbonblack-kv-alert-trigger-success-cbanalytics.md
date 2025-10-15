# Code Changes for vmware-carbonblack-kv-alert-trigger-success-cbanalytics (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'category', 'result', 'threat_id', 'time'] |
| edit_regex_field | threat_id |  | ['\WthreatAttackID=({alert_id}({threat_id}[^:]+?))\s*(\w+=|$|:)'] |
| added_regex_field | alert_id |  | ['\WthreatAttackID=({alert_id}({threat_id}[^:]+?))\s*(\w+=|$|:)'] |
| removed_attribute | DupFields |  | N/A |