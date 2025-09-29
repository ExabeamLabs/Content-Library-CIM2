# Code Changes for unix-unix-kv-email-send-success-smtp (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['bytes', 'email_address', 'email_domain', 'host', 'login_id', 'message_id', 'process_name', 'user'] |
| added_regex_field | login_id |  | ['sSMTP\[({login_id}\d+)'] |
| added_regex_field | process_name |  | ['({process_name}sSMTP)'] |