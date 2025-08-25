# Code Changes for tenable-t-sk4-alert-trigger-success-dcerpcservice-1 (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| changed | Conditions | ['"hostname":', '"publication_date":', '"scan":', '"started_at":', '"synopsis":'] | ['"exploit_available":', '"hostname":', '"indexed":', '"publication_date":', '"scan":', '"synopsis":'] |
| changed_parsed_fields | N/A | ['additional_info', 'alert_name', 'alert_severity', 'alert_status', 'cve_id', 'cvss_base_score', 'exploit_code_maturity', 'host', 'original_risk_score', 'protocol', 'see_also', 'solution', 'src_ip', 'src_port', 'time'] | ['additional_info', 'alert_name', 'alert_severity', 'alert_status', 'alert_subject', 'cve_id', 'cvss_base_score', 'exploit_code_maturity', 'host', 'original_risk_score', 'protocol', 'see_also', 'solution', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | time | ['started_at"+:\s*"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)'] | ['"indexed"+:\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)', 'started_at"+:\s*"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)'] |
| added_regex_field | alert_subject | [] | ['"synopsis"+:\s*"+({alert_subject}[^"]+)'] |
| added_attribute | DupFields | N/A | ['alert_name->alert_type'] |