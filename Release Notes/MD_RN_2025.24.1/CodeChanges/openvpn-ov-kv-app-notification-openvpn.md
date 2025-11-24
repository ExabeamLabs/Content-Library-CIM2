# Code Changes for openvpn-ov-kv-app-notification-openvpn (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_port', 'failure_reason', 'host', 'process_id', 'src_host', 'time'] |
| edit_regex_field | dest_port |  | ['({src_host}({host}[\w.\-]+))\s+openvpn\[({dest_port}\d+)\]'] |
| edit_regex_field | host |  | ['({src_host}({host}[\w.\-]+))\s+openvpn\[({dest_port}\d+)\]'] |
| added_regex_field | src_host |  | ['({src_host}({host}[\w.\-]+))\s+openvpn\[({dest_port}\d+)\]'] |
| removed_attribute | DupFields |  | N/A |