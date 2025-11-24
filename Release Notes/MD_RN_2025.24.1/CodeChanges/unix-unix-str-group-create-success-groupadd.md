# Code Changes for unix-unix-str-group-create-success-groupadd (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'dest_host', 'group_name', 'host', 'host_ip', 'process_id', 'process_name', 'provider_name'] |
| edit_regex_field | host |  | ['\d\d:\d\d:\d\d(\.\S+)? ({dest_host}({host}[\w.\-]+))\sgroupadd', '\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log|({=host}[\w.\-]+)\s)?'] |
| added_regex_field | dest_host |  | ['\d\d:\d\d:\d\d(\.\S+)? ({dest_host}({host}[\w.\-]+))\sgroupadd'] |
| removed_attribute | DupFields |  | N/A |