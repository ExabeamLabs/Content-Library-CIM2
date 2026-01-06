# Code Changes for checkpoint-ngfw-kv-app-activity-newantivirus (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'action', 'additional_info', 'alert_name', 'app_protocol', 'bytes', 'bytes_in', 'bytes_out', 'dest_host', 'dest_ip', 'dest_port', 'dest_translated_ip', 'dest_translated_port', 'direction', 'domain', 'end_time', 'event_name', 'failure_reason', 'first_name', 'full_name', 'host', 'last_name', 'operation', 'origin_ip', 'origin_name', 'product_name', 'protocol', 'result', 'rule', 'rule_id', 'rule_type', 'severity', 'src_host', 'src_interface', 'src_ip', 'src_port', 'src_translated_ip', 'src_translated_port', 'start_time', 'time', 'user', 'user_ou'] |
| edit_regex_field | domain |  | ['\Wdst_machine_name:"({dest_host}[^"@]+)@({domain}[^"]+)', '\Wsrc_machine_name:"({src_host}[^"@]+)@({domain}[^"]+)', 'domain:"({domain}[^"]+)'] |
| edit_regex_field | event_name |  | ['\Waction:"({event_name}[^"]+)', 'event_name:"({event_name}[^"]+)'] |
| edit_regex_field | rule_id |  | ['\Wapp_rule_id:"\{({rule_id}[^"\}]+)', '\Wrule_uid:"\{?({rule_id}[^"\}]+)', 'cu_rule_id"?:"({rule_id}[^"]+)'] |
| added_regex_field | bytes_in |  | ['\Wreceived_bytes:\"+({bytes_in}\d+)'] |
| added_regex_field | bytes_out |  | ['\Wsent_bytes:\"+({bytes_out}\d+)'] |
| added_regex_field | direction |  | ['ifdir:"({direction}[^"]+)'] |
| added_regex_field | end_time |  | ['event_end_time:"({end_time}\d{10})'] |
| added_regex_field | rule_type |  | ['cu_rule_category:"({rule_type}[^"]+)'] |
| added_regex_field | start_time |  | ['event_start_time:"({start_time}\d{10})'] |
| changed | Conditions |  | ['ifdir:"', 'origin:"', 'origin_sic_name:"', 'product:"New Anti Virus"', 'severity:"'] |
| added_attribute | start_timeFormat |  | epoch_sec |
| added_attribute | end_timeFormat |  | epoch_sec |