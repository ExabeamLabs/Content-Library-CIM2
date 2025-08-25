# Code Changes for cisco-fp-kv-alert-trigger-success-acpolicy (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_name', 'alert_severity', 'alert_type', 'dest_ip', 'dest_port', 'egress_interface', 'host', 'ingress_interface', 'protocol', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | action |  | ['InlineResult:\s*({action}[^,"]+)'] |