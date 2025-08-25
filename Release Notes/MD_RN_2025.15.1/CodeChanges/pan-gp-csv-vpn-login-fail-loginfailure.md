# Code Changes for pan-gp-csv-vpn-login-fail-loginfailure (Parser)

| Code Change | Field Name | 2025.14.1 | 2025.15.1 |
|-------------|------------|-----------|------------|
| edit_regex_field | additional_info | [',(|\s*({failure_reason}[^,]+?)\s*"*\s*),(""+|"({additional_info}[^"]+)"),({result}failure)', 'GLOBALPROTECT,([^,]*,){19}("+,|"+[^"]+"+,)([^,]*,){3}("+,|"+({additional_info}[^"]+)"+,)'] | [',(|\s*({failure_reason}[^,]+?)\s*"*\s*),(""+|"({additional_info}[^"]+)"),({result}failure)', ',GLOBALPROTECT,([^,]*,){19}("+,|"+[^"]+"+,)([^,]*,){3}("+,|"+({additional_info}[^"]+)"+,)'] |
| edit_regex_field | auth_type | ['GLOBALPROTECT,([^,]*,){6}(|({auth_type}[^,]*)),'] | [',GLOBALPROTECT,([^,]*,){6}(|({auth_type}[^,]*)),'] |
| edit_regex_field | device_type | ['GLOBALPROTECT,([^,]*,){19}"*(|({device_type}[^=]+?))"*\s*,'] | [',GLOBALPROTECT,([^,]*,){19}"*(|({device_type}[^=]+?))"*\s*,'] |
| edit_regex_field | os | ['GLOBALPROTECT,([^,]*,){18}(|(?i)any|({os}[^,]*)),'] | [',GLOBALPROTECT,([^,]*,){18}(|(?i)any|({os}[^,]*)),'] |
| edit_regex_field | result | [',(|\s*({failure_reason}[^,]+?)\s*"*\s*),(""+|"({additional_info}[^"]+)"),({result}failure)', 'GLOBALPROTECT,([^,]*,){19}("+,|"+[^"]+"+,)([^,]*,){3}("+,|"+[^"]+"+,)({result}failure|success)'] | [',(|\s*({failure_reason}[^,]+?)\s*"*\s*),(""+|"({additional_info}[^"]+)"),({result}failure)', ',GLOBALPROTECT,([^,]*,){19}("+,|"+[^"]+"+,)([^,]*,){3}("+,|"+[^"]+"+,)({result}failure|success)'] |
| edit_regex_field | src_host | ['GLOBALPROTECT,([^,]*,){10}({src_host}[\w\-\.]+)'] | [',GLOBALPROTECT,([^,]*,){10}({src_host}[\w\-\.]+)'] |
| edit_regex_field | src_mac | ['GLOBALPROTECT,([^,]*,){15}({src_mac}([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})'] | [',GLOBALPROTECT,([^,]*,){15}({src_mac}([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})'] |