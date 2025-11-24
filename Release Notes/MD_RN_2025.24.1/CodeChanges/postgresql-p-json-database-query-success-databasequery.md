# Code Changes for postgresql-p-json-database-query-success-databasequery (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['db_user', 'src_ip', 'src_port', 'user'] |
| edit_regex_field | user |  | ['exa_json_path=$.user_name,exa_regex=({db_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| added_regex_field | db_user |  | ['exa_json_path=$.user_name,exa_regex=({db_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| removed_attribute | DupFields |  | N/A |