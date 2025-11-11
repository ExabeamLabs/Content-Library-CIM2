# Code Changes for windows-events-2 (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'domain', 'event_code', 'login_id', 'login_type', 'process_dir', 'process_id', 'process_name', 'process_path', 'provider_name', 'src_port', 'time', 'user_sid'] |
| edit_regex_field | domain |  | ['"new_logon.account_domain"+:"+({domain}[^"]+)'] |
| removed_regex_field | user |  | [] |
| removed_regex_field | user_upn |  | [] |