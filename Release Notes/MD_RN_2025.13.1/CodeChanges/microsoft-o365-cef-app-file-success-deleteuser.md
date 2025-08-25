# Code Changes for microsoft-o365-cef-app-file-success-deleteuser (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'app_id', 'browser', 'category', 'correlation_id', 'dest_email_address', 'dest_email_domain', 'dest_ip', 'dest_port', 'dest_user', 'domain', 'email_address', 'email_domain', 'email_subject', 'event_name', 'failure_reason', 'file_name', 'first_name', 'full_name', 'group_name', 'host', 'key_name', 'last_name', 'object', 'operation', 'operation_type', 'os', 'process_name', 'resource', 'resource_id', 'result', 'secret', 'service_name', 'src_file_name', 'src_ip', 'src_port', 'time', 'user', 'user_agent', 'user_id', 'user_sid', 'user_type'] |
| removed_regex_field | file_dir |  | [] |
| removed_regex_field | file_ext |  | [] |
| edit_regex_field | file_name |  | ['((fileType=(n\/a|N\/A|mail|calendar-event|note|message)[^\n]*?\sfname=\s*(N\/A|({email_subject}[^=]+?)))|(fileType=group[^\n]*?\sfname=\s*(N\/A|({group_name}[^=]+?)))|(fileType=(file|folder|attachment|report)[^\n]*?\sfname=\s*(N\/A|({file_name}[^=]+?)))|(fileType=process[^\n]*?\sfname=\s*(N\/A|({process_name}[^=]+?)))|(fileType=app(lication)?[^\n]*?\sfname=\s*(N\/A|({app}[^=]+?)))|(fileType=secret[^\n]*?\sfname=\s*(N\/A|({secret}[^=]+?)))|(fileType=key[^\n]*?\sfname=\s*(N\/A|({key_name}[^=]+?))))\s+(\w+=|$)', 'DatasetName"*:\s*"*({file_name}[^"]+)'] |
| removed_regex_field | file_path |  | [] |
| added_regex_field | app_id |  | ['appId":"({app_id}[^"]+)"'] |