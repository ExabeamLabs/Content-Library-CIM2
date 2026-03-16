# Code Changes for github-g-json-app-activity-document_id (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'company', 'country_code', 'doc_id', 'domain', 'email_address', 'host', 'operation_type', 'src_ip', 'src_port', 'time', 'user', 'user_agent', 'user_id'] |
| edit_regex_field | email_address |  | ['"email":\s*"({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+.[^\]\s"\\,\|]+)"', 'exa_json_path=$..email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+.[^\]\s"\\,\|]+)', 'exa_json_path=$.external_identity_username,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | user |  | ['"user":\s*"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"', 'exa_json_path=$.external_identity_username,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| added_regex_field | action |  | ['"action":\s*"({action}[^"]+)"'] |
| added_regex_field | company |  | ['"business":\s*"({company}[^"]+)"'] |
| added_regex_field | country_code |  | ['"country_code":\s*"({country_code}[^"]+)"'] |
| added_regex_field | doc_id |  | ['"_document_id":\s*"({doc_id}[^"]+)"'] |
| added_regex_field | host |  | ['({host}\S+)\s+github_audit:'] |
| added_regex_field | operation_type |  | ['"operation_type":\s*"({operation_type}[^"]+)"'] |
| added_regex_field | src_ip |  | ['"actor_ip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"'] |
| added_regex_field | src_port |  | ['"actor_ip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"'] |
| added_regex_field | time |  | ['"@timestamp":({time}\d{13}),'] |
| added_regex_field | user_agent |  | ['"user_agent":\s*"({user_agent}[^"]+)"'] |
| added_regex_field | user_id |  | ['"user_id":\s*({user_id}\d+)'] |