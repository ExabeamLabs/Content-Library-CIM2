# Code Changes for microsoft-evsecurity-json-endpoint-login-success-4624-5 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'auth_process', 'dest_user', 'domain', 'host', 'login_id', 'login_type', 'process_path', 'src_host', 'src_host_windows', 'src_ip', 'src_port', 'user', 'user_sid'] |
| edit_regex_field | src_host_windows |  | ['exa_regex=Nom de la station de travail\\u00A0:\s*(-|\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({src_host_windows}({src_host}[\w\-\.]+)))\s*Adresse du r\\u00E9seau source\\u00A0:'] |
| added_regex_field | src_host |  | ['exa_regex=Nom de la station de travail\\u00A0:\s*(-|\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({src_host_windows}({src_host}[\w\-\.]+)))\s*Adresse du r\\u00E9seau source\\u00A0:'] |
| removed_attribute | DupFields |  | N/A |