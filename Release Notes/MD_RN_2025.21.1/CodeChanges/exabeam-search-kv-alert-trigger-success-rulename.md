# Code Changes for exabeam-search-kv-alert-trigger-success-rulename (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_id', 'alert_name', 'alert_reason', 'alert_type', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'event_id', 'event_time', 'host', 'log_time', 'malware_url', 'mitre_labels', 'original_risk_score', 'rule_description', 'rule_reason', 'rule_usecases', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | rule_reason |  | ['\Wrule_reason="({alert_reason}({rule_reason}[^"]+))'] |
| edit_regex_field | time |  | ['\Wevent_time="({event_time}({time}\d{13}))', 'timestamp="({event_time}({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d))'] |
| added_regex_field | alert_reason |  | ['\Wrule_reason="({alert_reason}({rule_reason}[^"]+))'] |
| added_regex_field | event_time |  | ['\Wevent_time="({event_time}({time}\d{13}))', 'timestamp="({event_time}({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d))'] |
| removed_attribute | DupFields |  | N/A |
| added_attribute | event_timeFormat |  | ['epoch', "yyyy-MM-dd'T'HH:mm:ss"] |