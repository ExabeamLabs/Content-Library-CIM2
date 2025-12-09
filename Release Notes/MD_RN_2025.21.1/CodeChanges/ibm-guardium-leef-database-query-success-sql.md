# Code Changes for ibm-guardium-leef-database-query-success-sql (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'additional_info', 'app', 'db_name', 'db_operation', 'db_query', 'db_user', 'dest_ip', 'dest_port', 'domain', 'host', 'protocol', 'rule_description', 'server_type', 'service_name', 'src_interface', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | db_user |  | ['\WdbUser=(({domain}[^\|\\]+)\\)?({account}({db_user}[^\|\\]+))'] |
| edit_regex_field | domain |  | ['\WdbUser=(({domain}[^\|\\]+)\\)?({account}({db_user}[^\|\\]+))'] |
| added_regex_field | account |  | ['\WdbUser=(({domain}[^\|\\]+)\\)?({account}({db_user}[^\|\\]+))'] |
| removed_attribute | DupFields |  | N/A |