# Code Changes for proofpoint-pitm-json-alert-trigger-success (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_severity', 'email_address', 'email_domain', 'file_dir', 'file_ext', 'file_name', 'file_path', 'src_ip'] |
| edit_regex_field | alert_severity |  | ['exa_json_path=$..intelligence.risk.overall.level,exa_regex=pfpt:risk:(\d+):({alert_severity}[^"]+)', 'exa_regex="risk":\{.+?"level":"[^}]+:((?i)none|null|({alert_severity}[^"]+))'] |
| edit_regex_field | email_address |  | ['exa_json_path=$.user.email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|0-9]+))', 'exa_regex=directory"+:\{.+?"+email"+:"+({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |
| edit_regex_field | email_domain |  | ['exa_json_path=$.user.email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|0-9]+))', 'exa_regex=directory"+:\{.+?"+email"+:"+({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |
| edit_regex_field | src_ip |  | ['exa_json_path=$..endpoint.location.ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))', 'exa_json_path=$.remote.host.ip.address,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))'] |
| added_regex_field | file_dir |  | ['exa_json_path=$.resources[0].path,exa_regex=({file_path}({file_dir}[^"]+[\\\/]+)?({file_name}[^\\\/"]+?(\.({file_ext}\w+))?))$'] |
| added_regex_field | file_ext |  | ['exa_json_path=$.resources[0].path,exa_regex=({file_path}({file_dir}[^"]+[\\\/]+)?({file_name}[^\\\/"]+?(\.({file_ext}\w+))?))$'] |
| added_regex_field | file_name |  | ['exa_json_path=$.resources[0].path,exa_regex=({file_path}({file_dir}[^"]+[\\\/]+)?({file_name}[^\\\/"]+?(\.({file_ext}\w+))?))$'] |
| added_regex_field | file_path |  | ['exa_json_path=$.resources[0].path,exa_regex=({file_path}({file_dir}[^"]+[\\\/]+)?({file_name}[^\\\/"]+?(\.({file_ext}\w+))?))$'] |