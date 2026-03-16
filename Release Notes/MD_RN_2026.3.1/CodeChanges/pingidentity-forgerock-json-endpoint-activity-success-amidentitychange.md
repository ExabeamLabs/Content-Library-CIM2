# Code Changes for pingidentity-forgerock-json-endpoint-activity-success-amidentitychange (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['exa_json_path=$..runAs,exa_regex=id=({user}[\w\.\-\!\#\^\~]{1,40}\$?),ou=user,dc=({domain}[^,]+),'] |
| edit_regex_field | object_id |  | ['exa_json_path=$..objectId,exa_regex=uid=({object_id}[^,]+),'] |
| edit_regex_field | user |  | ['exa_json_path=$..runAs,exa_regex=id=({user}[\w\.\-\!\#\^\~]{1,40}\$?),ou=user,dc=({domain}[^,]+),'] |