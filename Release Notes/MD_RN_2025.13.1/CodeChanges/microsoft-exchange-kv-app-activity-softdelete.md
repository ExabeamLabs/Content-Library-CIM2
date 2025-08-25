# Code Changes for microsoft-exchange-kv-app-activity-softdelete (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'attachment', 'email_address', 'email_attachments', 'email_domain', 'email_subject', 'host', 'login_type', 'message_id', 'object', 'operation', 'process_dir', 'process_name', 'result', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| removed_regex_field | process_path |  | [] |
| added_regex_field | process_dir |  | ['Path":"({process_dir}[^"]+?)\s*"'] |