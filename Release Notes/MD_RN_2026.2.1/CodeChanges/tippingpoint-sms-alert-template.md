# Code Changes for tippingpoint-sms-alert-template (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_name', 'alert_severity', 'dest_ip', 'dest_port', 'event_id', 'src_ip', 'src_port'] |
| removed_regex_field | event_code |  | [] |
| added_regex_field | event_id |  | ['\s+({event_id}[^\s]+)\s+00000001-0001-0001-0001-00000'] |