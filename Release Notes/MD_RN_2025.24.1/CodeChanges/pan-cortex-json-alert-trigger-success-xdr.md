# Code Changes for pan-cortex-json-alert-trigger-success-xdr (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed | Conditions |  | ['"alert_id":', '"alert_type":', '"event_type":', '"severity":', '"source":'] |
| changed_parsed_fields | N/A |  | ['dest_ip', 'dest_port', 'domain', 'email_address', 'email_domain', 'src_ip', 'src_port', 'user'] |
| edit_regex_field | domain |  | ['exa_regex=user_name":\[?"(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\\s,]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| edit_regex_field | user |  | ['exa_regex=user_name":\[?"(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\\s,]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| added_regex_field | dest_ip |  | ['exa_json_path=$.action_remote_ip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?'] |
| added_regex_field | dest_port |  | ['exa_json_path=$.action_remote_ip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?'] |
| added_regex_field | email_address |  | ['exa_regex=user_name":\[?"(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\\s,]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| added_regex_field | email_domain |  | ['exa_regex=user_name":\[?"(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\\s,]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| added_regex_field | src_ip |  | ['exa_json_path=$.action_local_ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| added_regex_field | src_port |  | ['exa_json_path=$.action_local_ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |