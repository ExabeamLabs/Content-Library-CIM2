# Code Changes for crowdstrike-falcon-sk4-app-activity-eventsimplename-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_name', 'aid', 'aip', 'cid', 'container_id', 'dest_ip', 'dest_port', 'dest_user', 'dns_query_flags', 'domain', 'email_address', 'event_code', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'hash_md5', 'hash_sha256', 'host', 'os', 'parent_process_id', 'process_command_line', 'process_id', 'src_host', 'src_ip', 'src_port', 'time', 'user', 'user_sid', 'user_uid'] |
| added_regex_field | host |  | ['ComputerName":"({host}[^"]+)'] |
| edit_attribute | activity_type |  | ['app-activity:success', 'endpoint-command:success', 'process-create:success', 'registry-modify:success'] |
| edit_attribute | legacy_activity_type |  | ['app-activity', 'process-created', 'registry-write'] |