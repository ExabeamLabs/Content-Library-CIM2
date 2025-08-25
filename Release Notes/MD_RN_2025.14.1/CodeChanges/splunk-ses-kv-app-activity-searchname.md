# Code Changes for splunk-ses-kv-app-activity-searchname (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| COULD_NOT_COMPARE | TimeFormat | epoch_sec | ['epoch_sec', 'epoch', 'MM/dd/yyyy HH:mm:ss'] |
| changed_parsed_fields | N/A | ['city', 'dest_ip', 'dest_port', 'event_code', 'host', 'src_ip', 'src_port', 'time'] | ['alert_id', 'alert_name', 'alert_severity', 'alert_type', 'city', 'dest_ip', 'dest_port', 'end_time', 'event_id', 'host', 'occured_time', 'src_ip', 'src_port', 'start_time', 'threat_url', 'time', 'trigger_time'] |
| removed_regex_field | event_code | ['orig_event_id="({event_code}[^"]+)"'] | [] |
| added_regex_field | alert_id | [] | ['\sIncident\sID="({alert_id}[^,"]+)",'] |
| added_regex_field | alert_name | [] | ['\ssearch_name="({alert_name}[^,"]+)",'] |
| added_regex_field | alert_severity | [] | ['\sseverity="({alert_severity}[^,"]+)",'] |
| added_regex_field | alert_type | [] | ['\sIncident\sName="({alert_type}[^,"]+)",'] |
| added_regex_field | end_time | [] | ['\sinfo_max_time="({end_time}\d{10})",'] |
| added_regex_field | event_id | [] | ['orig_event_id="({event_id}[^"]+)"'] |
| added_regex_field | occured_time | [] | ['\sIncident\sTime="({occured_time}\d\d\d\d-\d\d-\d\d)",'] |
| added_regex_field | start_time | [] | ['\sinfo_min_time="({start_time}\d{10})'] |
| added_regex_field | threat_url | [] | ['\sIncident\sURL="({threat_url}[^,"]+)",'] |
| added_regex_field | trigger_time | [] | ['\sinfo_search_time="({trigger_time}\d{10})'] |
| added_attribute | occured_timeFormat | N/A | yyyy-MM-dd |
| added_attribute | trigger_timeFormat | N/A | epoch_sec |
| added_attribute | start_timeFormat | N/A | epoch_sec |
| added_attribute | end_timeFormat | N/A | epoch_sec |