# Code Changes for crowdstrike-falcon-mix-alert-trigger-success-detectionsummaryevent (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'aid', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'bootup_safeguard_enabled', 'category', 'cid', 'critical_process_disabled', 'dest_ip', 'dest_port', 'detect', 'domain', 'falcon_host_link', 'file_dir', 'file_name', 'fs_operation_blocked', 'grandparent_command_line', 'grandparent_image_filename', 'hash_md5', 'hash_sha256', 'inddet_mask', 'indicator', 'kill_parent', 'kill_process', 'kill_sub_process', 'operation_blocked', 'parent_image_filename', 'parent_process_command_line', 'pattern_disposition_description', 'policy_disabled', 'process_blocked', 'process_command_line', 'quarantine_file', 'quarantine_machine', 'registry_operation_blocked', 'rooting', 'sensor_id', 'sensor_only', 'src_host', 'src_ip', 'src_port', 'technique', 'time', 'user'] |
| edit_regex_field | additional_info |  | ['"DetectDescription":"({additional_info}[^"]+)"', '"FalconHostLink\\*":\s*\\*"({additional_info}({falcon_host_link}[^"]+))', '"PatternDispositionDescription":"({additional_info}[^"]+)"'] |
| edit_regex_field | alert_type |  | ['"DetectName":"({technique}({alert_type}[^"]+))"', '"ExternalApiType":"({technique}({alert_type}[^"]+))"', '"Technique":"({technique}({alert_type}[^"]+))'] |
| edit_regex_field | falcon_host_link |  | ['"FalconHostLink\\*":\s*\\*"({additional_info}({falcon_host_link}[^"]+))'] |
| added_regex_field | technique |  | ['"DetectName":"({technique}({alert_type}[^"]+))"', '"ExternalApiType":"({technique}({alert_type}[^"]+))"', '"Technique":"({technique}({alert_type}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |