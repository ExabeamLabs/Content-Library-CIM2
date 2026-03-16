# Code Changes for pingidentity-forgerock-json-http-amsession (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['exa_json_path=$..userId,exa_regex=id=({user}[\w\.\-\!\#\^\~]{1,40}\$?),ou=user,o=({group_name}[^,]+),ou=services,dc=({domain}[^,]+),'] |
| edit_regex_field | group_name |  | ['exa_json_path=$..userId,exa_regex=id=({user}[\w\.\-\!\#\^\~]{1,40}\$?),ou=user,o=({group_name}[^,]+),ou=services,dc=({domain}[^,]+),'] |
| edit_regex_field | user |  | ['exa_json_path=$..userId,exa_regex=id=({user}[\w\.\-\!\#\^\~]{1,40}\$?),ou=user,o=({group_name}[^,]+),ou=services,dc=({domain}[^,]+),'] |