# Code Changes for crowdstrike-falcon-mix-alert-trigger-success-suspiciousactivity (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'additional_info_1', 'additional_info_2', 'alert_id', 'alert_name', 'alert_severity', 'alert_source', 'alert_subject', 'alert_type', 'category', 'cid', 'dest_host', 'dest_ip', 'dest_port', 'disposition', 'email_address', 'falcon_host_link', 'file_path', 'grandparent_command_line', 'grandparent_image_filename', 'hash_md5', 'hash_sha256', 'parent_image_filename', 'parent_process_command_line', 'parent_process_guid', 'process_command_line', 'process_guid', 'process_name', 'protocol', 'sensor_id', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | additional_info |  | ['"FalconHostLink":\s*"({additional_info}({falcon_host_link}[^"]+))"', '"PatternDispositionDescription":"({additional_info}[^"]+)"'] |
| edit_regex_field | alert_name |  | ['"DetectDescription":"({alert_name}[^"]+)"', '"DetectName":\s*"({alert_subject}({alert_name}({alert_type}[^"]+)))"', '"IOARuleName":"({alert_name}[^"]+)"', '"Technique":"({alert_subject}({alert_name}({alert_type}[^"]+)))'] |
| edit_regex_field | alert_type |  | ['"DetectName":\s*"({alert_subject}({alert_name}({alert_type}[^"]+)))"', '"Technique":"({alert_subject}({alert_name}({alert_type}[^"]+)))'] |
| edit_regex_field | falcon_host_link |  | ['"FalconHostLink":\s*"({additional_info}({falcon_host_link}[^"]+))"'] |
| added_regex_field | alert_subject |  | ['"DetectName":\s*"({alert_subject}({alert_name}({alert_type}[^"]+)))"', '"Technique":"({alert_subject}({alert_name}({alert_type}[^"]+)))'] |
| removed_attribute | DupFields |  | N/A |