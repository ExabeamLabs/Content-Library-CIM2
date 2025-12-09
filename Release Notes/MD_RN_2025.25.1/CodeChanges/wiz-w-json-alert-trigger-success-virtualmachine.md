# Code Changes for wiz-w-json-alert-trigger-success-virtualmachine (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| COULD_NOT_COMPARE | TimeFormat |  | ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"] |
| changed | Conditions |  | ['"cloudPlatform":"', '"name":"', '"severity":"', '"trigger":{"', '"type":"'] |
| changed_parsed_fields | N/A |  | ['app', 'src_ip'] |
| added_regex_field | src_ip |  | ['exa_json_path=$..triggeringEvents[0].actorIP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))'] |
| added_attribute | start_timeFormat |  | yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ |
| added_attribute | end_timeFormat |  | yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ |