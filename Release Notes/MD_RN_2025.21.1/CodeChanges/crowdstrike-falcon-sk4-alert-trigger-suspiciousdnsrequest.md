# Code Changes for crowdstrike-falcon-sk4-alert-trigger-suspiciousdnsrequest (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['aid', 'aip', 'alert_name', 'alert_subject', 'alert_type', 'cid', 'container_id', 'dns_query', 'event_code', 'host', 'os', 'src_ip', 'src_port', 'time', 'web_domain'] |
| edit_regex_field | event_code |  | ['"event_simpleName":"({alert_subject}({alert_type}({alert_name}({event_code}[^"]+))))'] |
| edit_regex_field | web_domain |  | ['"DomainName":"({dns_query}({web_domain}[^"]+))'] |
| added_regex_field | alert_name |  | ['"event_simpleName":"({alert_subject}({alert_type}({alert_name}({event_code}[^"]+))))'] |
| added_regex_field | alert_subject |  | ['"event_simpleName":"({alert_subject}({alert_type}({alert_name}({event_code}[^"]+))))'] |
| added_regex_field | alert_type |  | ['"event_simpleName":"({alert_subject}({alert_type}({alert_name}({event_code}[^"]+))))'] |
| added_regex_field | dns_query |  | ['"DomainName":"({dns_query}({web_domain}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |