# Code Changes for mimecast-seg-cef-app-login-fail-logonauthfailed (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'email_address', 'email_domain', 'failure_reason', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | app |  | ['\sApplication:\s*({app}[^,]+?),', 'exa_regex=\sApplication:\s*({app}[^,]+?),'] |
| edit_regex_field | email_address |  | ['"user":"({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))', '"user":"(|({email_address}[^@]+@[^"]+?))"', 'exa_json_path=$.user,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))', 'exa_json_path=$.user.email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |
| edit_regex_field | email_domain |  | ['"user":"({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))', 'exa_json_path=$.user,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))', 'exa_json_path=$.user.email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |
| edit_regex_field | failure_reason |  | ['\sReason:\s(|({failure_reason}[^=]+?))(\s+\w+=|\s*$)', 'exa_regex=\sReason:\s*(|({failure_reason}[^="]+?))(\s+\w+:|\s*")'] |
| edit_regex_field | src_ip |  | ['IP:\s({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}),', 'exa_regex=\WIP:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| added_regex_field | src_port |  | ['exa_regex=\WIP:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |