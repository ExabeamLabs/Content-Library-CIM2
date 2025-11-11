# Code Changes for mcafee-es-csv-alert-trigger-success-epolicyorchestrator (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_name', 'alert_severity', 'alert_type', 'domain', 'host', 'malware_url', 'process_name', 'process_path', 'src_host', 'threat_category', 'time', 'user'] |
| edit_regex_field | host |  | ['ePOEvents([^,]*,){13}["\']*({src_host}({host}[\w\-.]+))'] |
| added_regex_field | src_host |  | ['ePOEvents([^,]*,){13}["\']*({src_host}({host}[\w\-.]+))'] |
| removed_attribute | DupFields |  | N/A |