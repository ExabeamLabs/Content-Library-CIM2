# Code Changes for trendmicro-tippingpoint-str-alert-trigger-success-http (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_id', 'alert_name', 'alert_severity', 'dest_ip', 'dest_port', 'dest_zone', 'event_id', 'hit_cnt', 'host', 'protocol', 'src_ip', 'src_port', 'src_zone_name', 'time', 'vlan_id'] |
| removed_regex_field | event_code |  | [] |
| added_regex_field | event_id |  | ['\s+({event_id}[^\s]+)\s+00000001-0001-0001-0001-00000'] |