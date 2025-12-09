# Code Changes for zscaler-ia-json-network-traffic-success-internalreason (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'app_group', 'app_learntime', 'bytes_in', 'bytes_out', 'ca_runtime', 'connection_id', 'connection_status', 'dest_host', 'dest_ip', 'dest_port', 'email_address', 'event_start_time', 'event_stop_time', 'host', 'host_ip', 'operation_type', 'policy_name', 'policy_runtime', 'protocol', 'result', 'result_reason', 'rx_client_total_bytes', 'rx_connector_total_bytes', 'session_id', 'src_country', 'src_ip', 'src_port', 'time', 'tx_client_total_bytes', 'tx_connector_total_bytes', 'user', 'zen_code', 'zen_con_code'] |
| edit_regex_field | app_group |  | ['"AppGroup":\s*"({operation_type}({app_group}[^"]+))"'] |
| edit_regex_field | result |  | ['ConnectionStatus":\s*"({connection_status}({result}[^"]+))"'] |
| edit_regex_field | rx_connector_total_bytes |  | ['"ZENTotalBytesRxConnector":\s*({rx_connector_total_bytes}({bytes_in}\d+))'] |
| edit_regex_field | tx_connector_total_bytes |  | ['"ZENTotalBytesTxConnector":\s*({tx_connector_total_bytes}({bytes_out}\d+))'] |
| added_regex_field | bytes_in |  | ['"ZENTotalBytesRxConnector":\s*({rx_connector_total_bytes}({bytes_in}\d+))'] |
| added_regex_field | bytes_out |  | ['"ZENTotalBytesTxConnector":\s*({tx_connector_total_bytes}({bytes_out}\d+))'] |
| added_regex_field | connection_status |  | ['ConnectionStatus":\s*"({connection_status}({result}[^"]+))"'] |
| added_regex_field | operation_type |  | ['"AppGroup":\s*"({operation_type}({app_group}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |