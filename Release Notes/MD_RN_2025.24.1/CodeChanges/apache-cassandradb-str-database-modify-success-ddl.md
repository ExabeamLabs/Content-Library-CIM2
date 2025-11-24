# Code Changes for apache-cassandradb-str-database-modify-success-ddl (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'db_name', 'db_operation', 'db_query', 'db_user', 'dest_ip', 'dest_port', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | additional_info |  | ['\|operation:({db_query}({additional_info}[^|\.]+))', '\|operation:({db_query}({additional_info}[^|]+?))\s*$'] |
| added_regex_field | db_query |  | ['\|operation:({db_query}({additional_info}[^|\.]+))', '\|operation:({db_query}({additional_info}[^|]+?))\s*$'] |
| removed_attribute | DupFields |  | N/A |