# Code Changes for sophos-ep-sk4-app-notification-success-scheduleddailylimitexceeded (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'domain', 'event_name', 'full_name', 'host', 'malware_url', 'os', 'process_name', 'process_path', 'src_host', 'src_ip', 'src_port', 'target', 'time', 'user'] |
| edit_regex_field | alert_name |  | ['"name":"({event_name}({alert_name}[^"]+))', '"name":\s*"(n\/a|({event_name}({alert_name}[^\:\"\\']+(\:\s*\\'({target}[^\"\\']+))?\\')))', '"threat":"?(null|({event_name}({alert_name}[^",]+)))', '"type":"({alert_name}[^"]+)"', '"type":"({event_name}({alert_name}Event::Endpoint::[^"]+))'] |
| edit_regex_field | host |  | ['"location":"({src_host}({host}((\d{1,3}\.){3}\d{1,3}|({=src_host}[\w\-.]+))))"'] |
| edit_regex_field | src_host |  | ['"location":"({src_host}({host}((\d{1,3}\.){3}\d{1,3}|({=src_host}[\w\-.]+))))"'] |
| edit_regex_field | target |  | ['"name":\s*"(n\/a|({event_name}({alert_name}[^\:\"\\']+(\:\s*\\'({target}[^\"\\']+))?\\')))'] |
| added_regex_field | event_name |  | ['"name":"({event_name}({alert_name}[^"]+))', '"name":\s*"(n\/a|({event_name}({alert_name}[^\:\"\\']+(\:\s*\\'({target}[^\"\\']+))?\\')))', '"threat":"?(null|({event_name}({alert_name}[^",]+)))', '"type":"({event_name}({alert_name}Event::Endpoint::[^"]+))', '"type":"({event_name}[^"]+)"'] |
| removed_attribute | DupFields |  | N/A |