# Code Changes for pingidentity-forgerock-json-endpoint-authentication-amlogin (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['exa_json_path=$..userId,exa_regex=id=({user}[\w\.\-\!\#\^\~]{1,40}\$?),ou=user,o=({group_name}[^,]+),ou=services,dc=({domain}[^,]+),'] |
| edit_regex_field | group_name |  | ['exa_json_path=$..userId,exa_regex=id=({user}[\w\.\-\!\#\^\~]{1,40}\$?),ou=user,o=({group_name}[^,]+),ou=services,dc=({domain}[^,]+),'] |
| edit_regex_field | src_ip |  | ['exa_json_path=$..entries[0].info.ipAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| edit_regex_field | src_port |  | ['exa_json_path=$..entries[0].info.ipAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| edit_regex_field | user |  | ['exa_json_path=$..userId,exa_regex=id=({user}[\w\.\-\!\#\^\~]{1,40}\$?),ou=user,o=({group_name}[^,]+),ou=services,dc=({domain}[^,]+),'] |