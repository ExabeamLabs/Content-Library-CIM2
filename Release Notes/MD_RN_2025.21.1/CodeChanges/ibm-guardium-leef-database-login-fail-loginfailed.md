# Code Changes for ibm-guardium-leef-database-login-fail-loginfailed (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'db_name', 'db_user', 'dest_ip', 'dest_port', 'domain', 'host', 'result_reason', 'rule_description', 'server_type', 'src_interface', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | db_user |  | ['\WdbUser=(({domain}[^\|\\]+)\\)?(\?|({account}({db_user}[^\|\\]+)))'] |
| edit_regex_field | domain |  | ['\WdbUser=(({domain}[^\|\\]+)\\)?(\?|({account}({db_user}[^\|\\]+)))'] |
| added_regex_field | account |  | ['\WdbUser=(({domain}[^\|\\]+)\\)?(\?|({account}({db_user}[^\|\\]+)))'] |
| removed_attribute | DupFields |  | N/A |