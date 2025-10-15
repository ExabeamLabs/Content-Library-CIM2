# Code Changes for oracle-db-mix-database-query-success-audit (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'db_id', 'db_operation', 'db_query', 'db_user', 'dest_user', 'host', 'privileges', 'time', 'user'] |
| edit_regex_field | account |  | ["\sDATABASE USER:\[\d+\]\s*'(\/|({db_user}({account}[^'\\/\s]+)))'"] |
| added_regex_field | db_user |  | ["\sDATABASE USER:\[\d+\]\s*'(\/|({db_user}({account}[^'\\/\s]+)))'"] |
| removed_attribute | DupFields |  | N/A |