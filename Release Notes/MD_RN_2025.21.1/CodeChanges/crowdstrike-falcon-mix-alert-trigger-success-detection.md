# Code Changes for crowdstrike-falcon-mix-alert-trigger-success-detection (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'additional_info_1', 'additional_info_2', 'aid', 'alert_description', 'alert_id', 'alert_name', 'alert_severity', 'alert_source', 'alert_subject', 'alert_type', 'bootup_safeguard_enabled', 'cid', 'critical_process_disabled', 'dest_host', 'dest_ip', 'dest_port', 'detect', 'disposition', 'domain', 'email_address', 'email_domain', 'falcon_host_link', 'file_dir', 'file_ext', 'file_name', 'file_path', 'fs_operation_blocked', 'grandparent_command_line', 'grandparent_image_filename', 'hash_md5', 'hash_sha256', 'host', 'inddet_mask', 'indicator', 'ioc', 'kill_parent', 'kill_process', 'kill_sub_process', 'malware_url', 'operation_blocked', 'parent_image_filename', 'parent_process_command_line', 'pattern_disposition_description', 'policy_disabled', 'process_blocked', 'process_command_line', 'process_name', 'protocol', 'quarantine_file', 'quarantine_machine', 'registry_operation_blocked', 'rooting', 'sensor_id', 'sensor_only', 'src_host', 'src_ip', 'src_port', 'src_product', 'time', 'user'] |
| edit_regex_field | additional_info |  | ['"Description":"({additional_info}[^"]+)"', '"DetectDescription":\s*"\s*({additional_info}({alert_description}[^"]+?))\s*"'] |
| edit_regex_field | alert_description |  | ['"DetectDescription":\s*"\s*({additional_info}({alert_description}[^"]+?))\s*"'] |
| edit_regex_field | alert_name |  | ['"Technique":"({alert_subject}({alert_name}[^"]+))"'] |
| edit_regex_field | falcon_host_link |  | ['"FalconHostLink":\s*"({malware_url}({falcon_host_link}[^"]+))"'] |
| added_regex_field | alert_subject |  | ['"Technique":"({alert_subject}({alert_name}[^"]+))"'] |
| added_regex_field | malware_url |  | ['"FalconHostLink":\s*"({malware_url}({falcon_host_link}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |